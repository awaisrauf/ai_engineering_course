---
layout: note
title: "Lecture 6: Fine-tuning, Datasets and Hardware"
lecture: 1
date: 2026-06-02
---


- Structure of this lecture
    1. Rely on unsloth for finetuning
    2. case for finetuning → hardware → sft → rlhf
    3. unsloth based experimentation 
- [https://tinker-docs.thinkingmachines.ai/tutorials/](https://tinker-docs.thinkingmachines.ai/tutorials/)

So far, we have studied how to use large language models (LLMs) with in-context learning and how to build scafolding around LLMs to make them more useful. However, in many cases, using fixed model alone may not be sufficient for this. In such cases, you need to update model weights on dataset designed for specific task. 

In this lecture, you will learn how to update (finetune) model weights to add knowledge or certain behaviour. However, it is expensive and require memory footprint. We will start with 1) when fine-tuning makes sense, 2) hardware math for fine-tuning 3) finetuning types 4) SFT 5) Reinforcement-based Fine-tuning

## Why and When to fine-tune

### Reasons for Fine-tuning

Finetuning is updating a pre-trained model’s weight to improve. For LLM, fine-tuning can be used for following purposes. 

1. **Instruction-following:** Enable model to accurately follow user instructions, improve its tone, personality, or response style. For example, OpenAI initially did for xx. 
2. **Injecting Domain-specific Knowledge:** Adding knowledge of a domain. Example: xx
3. **Task-Specific Capabilities Improvements: I**mproving model’s capablities on specific tasks. For instance, a small models may not be able to produce a specific dialetic of SQL. 
4. Tool calling? 
5. **Distillation:** Distilling capabilities of a larger model. For instance, deepseek, qwen’s claude example 

### When to Fine-tune

You should not directly go to finetuning just because you can. You should first exhaust cheaper options. Here is how you should determine if you need finetuning

1. First define evaluation criteria, design eval data, etc (follow lecture 2) 
2. Experiment with prompt engineering
    1. Try different prompts
    2. Add more examples (1-50 examples)
3. If model fails
    1. If model fails because of information, connect it with right data sources (RAG lecture)
    2. If model failure are very specific (e.g., math-related), try adding tools or memory helps
    3. If model fails because of behavioural or missing of domain specific knowledge → finetune

Remember, finetuning also means that you will have to host the inference yourself, which may add to the complexity. It is hard to acquiring data, maintaining models, observing, serving and xx. 

### Examples of Finetuning Cases

Enable LLM to predict a headline’s impact is positive

Change the tone of an LLM to sound like Mideval English sailor in all it’s ocnverations 

xxx

## Finetuning Hardware Math

Once you have decided to finetune the model, you need to consider resources. LLM finetuning require computation but it is more memory-bind. In other words, you are primarily limited by the amount of VRAM you have. Hence, it is important to understand memory requirements. 

LLMs are transformer models. The training memory requirement is based on following 

( weights + activations + gradients + optimizer state )* numerical representaiotn. 

here need to add a figure. 

**Example**: 

**Example**: 

## Finetuning

When you know how output looks like vs. when you do not know (e.g., less toxic, tone more warm) and can only collect preference.

Now that you have understood what kind of model you finetune on your hardware, lets proceed with how to actually finetune a model. 

### Problem and Dataset and Model Selection

The first step for training or finetuning any machine learning model is to define the problem you are solving and gathering data for the problem, and divide them into train and validation splits. We will follow same loop here as well. However, the difference is that since LLMs are language models, we have more liberty with range of problems. Example: for sentiment analysis, traditional machine learning was strictly with constrained with set of emotions, with LLM, you can have more xx. 

Finetuning is the easier part. The hard part is selection of right model, gathering dataset, and other factors. Before diving deep into the finetuning, lets first go through steps. [TODO: read more from [OpenAI](https://developers.openai.com/api/docs/guides/fine-tuning-best-practices)’s guide. 

1. As previously, set the problem you are solving, define evaluation criteria to track the progress and xxx
2. **Select Base Model:** Select a base model based on memory math and your in-context learning. 
3. **Gather Training Data:**  
4. Iterate over Hyperparamters 

Before delving deep into the actual finetuning, lets first see what actual happens in the language model. 

### Supervised Finetuning or Instruction Tuning

Given input ($x$) and output ($y$), the supervised finetuning updates weights $W$ of LLM ($f$such that using a loss functions. 

In supervised fine tuning of LLMs, the loss function is cross entropy over wdords

$\mathcal{L}_{SFT} = \log (correct word)$

The LLM (or $f_{W}$) outputs logits distribution for each word. Assuming that the logit distribution for current word $i$ is $y_i$ then, we can compute the loss as follows. 

$\mathcal{L} = - \sum_i \log(y_i)$

With this loss, we learn the parameters $W$ of the LLM such that this loss is minimized. For the minimization, we use simple gradient descent.

[TODO: EXAMPLE, based on alpaca]

[TODO: Mention actual fine-tuning does not require sequential generation which makes it faster]

[TODO: Multi-turn training]

### PEFT Finetuning

While supervised finetuning can instill knowledge or change the behaviour as we want, it requires high amount of GPU VRAM. [TODO: Add a vram exmaple]. How can we fine tuning without needing huge VRAM. A naive first method could be just training last few layers. However, it is not as effective for reasons [TODO]. 

This is where Parameter Efficient Fine tuning comes into play, first introduced by xx. The Low Rank Adaptation (LoRA) is based on mathematical idea that the high dimensional weights of a LLM actually lives in low intrinsic dimension. And the weight updates during finetuning also lives in lower dimensional spaces. This means that we can update a lower rank approximation of weights to get the same effect as original weight $W$. 

To understand this idea more deeply, think of any intermiedate layer of an LLM producing taking an input vector $x$ and producing $h$ output by $h=W\cdot x$. As shown below.

[TODO: Add figure]

But instead of updating $W$ completely, in LoRA, we first decompose W into smaller, lower dimensional multiplication. So, think of W = B. A, as shown below. Both B and A are significnalty smaller. For instance, if W is 1000x1000 weight matrix. B and A could be 1000x10 and 10x1000.  

[TODO: Add figure]

 During training, we only update B and A, and use it to udpate original weight W by multiplying $\Delta W = B \cdot A$. Finally, we combine original weight with this weight to get updated weights such that 

$W_{updated} = W + \Delta W$

![image.png](Lecture%206%20Fine-tuning,%20Datasets%20and%20Hardware/image.png)

[TODO: Add figure]

[TODO: add exmpale for why it is significantly cheaper]

[TODO: Add exercise to calculate ram requirements with and without LoRA]

#### Practical Considerations

```
LoRA works as follows. Given a weight matrix $$W$$ with dimension $$n\times m$$, 

1. Select an intermeidate dimenstion $$r$$, choose two matrices $$W_A$$ of dim $$n \times r$$ and $$W_B$$ of dim $$r \times m$$. The product of these two is $$W_{AB}$$ of dim $$n\times m$$. Where, $$r$$ is rank of LoRA. 

2. During training, use $$W^{'}=W+\dfrac{\alpha}{r} W_{AB}$$, where $$\alpha$$ is a hyperparmater to determine contribution of $$W_{AB}$$ in weights.

3. During training, only update $$W_A$$ and $$W_B$$.
4. During inference merge and use $$W^{'}$$.

LoRA is most commonly applied to weight matrices of attention (query, key, value, and projection matrices). LoRA could be applied to specific attention layers and specific parts (e.g., only query matrix) based on the training budget. The LoRA rank $$r$$ also depend on the computation budget and an $$r$$ of between 4 and 64 is sufficient. The ratio a/r depends on use cases but larger r could mean smaller alpha and vice versa.

LoRA allows to efficiently serve multiple specialized models without need to store large amounts of weights.
```

Other training efficiency methods

1. CPU Offloading: [https://dl.acm.org/doi/10.1145/3394486.3406703](https://dl.acm.org/doi/10.1145/3394486.3406703)
2. Parameter Quaniztioan: 

### Distillation

Another challenging aspect of the finetuning is data and how to get it. Distillation. 

[TODO: Use a actual paper (e.g., deepseek or Alpaca) where authors used a template to generate questions answer and train model]. 

**Alpaca: A Strong, Replicable Instruction‑Following Model** — *Stanford 2023*

[https://arxiv.org/abs/2604.01193](https://arxiv.org/abs/2604.01193)

[TODO: Focus on data generation process]

[TODO: Example of success]

### Preference Optimization - DPO

May be not required. 

Based on this paper: [https://arxiv.org/pdf/2305.18290](https://arxiv.org/pdf/2305.18290)

### Reinforcement learning with Human Feedback

Finetuning 

Training language models to follow instructions with human feedback

[https://cameronrwolfe.substack.com/p/grpo](https://cameronrwolfe.substack.com/p/grpo)

# Resources

1. https://developers.openai.com/api/docs/guides/fine-tuning-best-practices
2. Finetuning gemma: [https://colab.research.google.com/github/unslothai/unsloth/blob/main/studio/Unsloth_Studio_Colab.ipynb](https://colab.research.google.com/github/unslothai/unsloth/blob/main/studio/Unsloth_Studio_Colab.ipynb)

# Related Papers

Training language models to follow instructions with human feedback -- SFT + RLHF alignment pipeline

Self-Instruct: Aligning Language Models with Self-Generated Instructions -- synthetic instruction data generation

Alpaca: A Strong, Replicable Instruction-Following Model -- low-cost instruction tuning via distillation

LoRA: Low-Rank Adaptation of Large Language Models -- parameter-efficient fine-tuning via low-rank updates

QLoRA: Efficient Finetuning of Quantized LLMs -- LoRA with quantization for low memory

Distilling the Knowledge in a Neural Network -- teacher-student model compression framework .S

LIMA: Less Is More for Alignment -- small high-quality data beats scale

Direct Preference Optimization: Your Language Model is Secretly a Reward Model -- preference learning without RL or reward model

RRHF: Rank Responses to Align Language Models -- ranking-based alignment without RL

ORPO: Monolithic Preference Optimization without Reference Model -- unified SFT and preference optimization

Deep Reinforcement Learning from Human Preferences -- learning rewards from human comparisons

Proximal Policy Optimization Algorithms -- stable policy gradient optimization method

Group Relative Policy Optimization -- group-based RL without reward model