---
layout: talk
# title: "Guest Lecture - Multimodal AI by Dr. Hira Dhamyal"
# lecture: "Guest"
# date: 2026-06-24
---

<style>
.talk-title-card {
  padding: 18px 0;
  margin: 20px 0 16px 0;
  text-align: center;
}

.talk-title-card h1 {
  color: #8F0E20;
  font-size: 2.1rem;
  margin: 0 0 8px 0;
  border: none;
}

.talk-title-card .talk-type {
  color: #8F0E20;
  font-weight: 300;
}

.talk-title-card .talk-subtitle {
  color: #444;
  font-size: 1.25rem;
  font-weight: 400;
  margin: 0;
}

.guest-hero {
  background: linear-gradient(135deg, #8F0E20 0%, #a61228 50%, #8F0E20 100%);
  border-radius: 14px;
  padding: 18px 24px;
  margin: 0 0 24px 0;
  color: white;
  display: flex;
  gap: 22px;
  align-items: center;
  max-width: 100%;
  box-shadow: 0 6px 20px rgba(143, 14, 32, 0.15);
}

.guest-hero .speaker-photo {
  width: 170px;
  height: 170px;
  border-radius: 50%;
  object-fit: cover;
  border: 3px solid rgba(255,255,255,0.9);
  box-shadow: 0 4px 16px rgba(0,0,0,0.2);
  flex-shrink: 0;
}

.guest-hero .speaker-info {
  flex: 1;
  min-width: 200px;
}

.guest-hero .speaker-info h2 {
  font-size: 1.9rem;
  margin: 0 0 6px 0;
  font-weight: 700;
  color: white;
  border: none;
}

.guest-hero .speaker-info .speaker-role {
  font-size: 1.2rem;
  opacity: 0.95;
  line-height: 1.5;
  margin-bottom: 12px;
  text-align: justify;
  hyphens: auto;
  -webkit-hyphens: auto;
  -ms-hyphens: auto;
  word-break: break-word;
}

.guest-hero .speaker-info .speaker-affiliations {
  display: flex;
  gap: 6px;
  flex-wrap: wrap;
}

.guest-hero .speaker-info .speaker-affiliations span {
  background: rgba(255,255,255,0.2);
  padding: 5px 14px;
  border-radius: 20px;
  font-size: 0.9rem;
  border: 1px solid rgba(255,255,255,0.3);
}

.guest-hero .speaker-logos {
  display: flex;
  flex-direction: row;
  gap: 14px;
  align-items: center;
  flex-shrink: 0;
}

.guest-hero .speaker-logos img {
  width: 90px;
  height: 90px;
  object-fit: contain;
  border-radius: 10px;
  background: white;
  padding: 10px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.15);
}

.event-card {
  background: #faf5f6;
  border: 1px solid #f0e0e3;
  border-radius: 12px 12px 0 0;
  padding: 14px 24px;
  margin: 0;
  display: flex;
  justify-content: center;
  gap: 8px;
  align-items: center;
  font-size: 1.05rem;
  color: #333;
}

.event-card .event-item {
  display: flex;
  align-items: center;
  gap: 5px;
}

.event-card .event-label {
  font-weight: 600;
  color: #8F0E20;
}

.event-card .event-sep {
  color: #ccc;
  margin: 0 4px;
}

.register-block {
  background: #faf5f6;
  border: 1px solid #f0e0e3;
  border-top: none;
  border-radius: 0 0 12px 12px;
  padding: 8px 24px;
  margin: 0 0 24px 0;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 8px;
}

.register-block p {
  margin: 0;
  color: #555;
  font-size: 1.05rem;
}

.register-block a {
  display: inline-block;
  background: #8F0E20;
  color: white !important;
  padding: 7px 20px;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  font-size: 1.05rem;
  transition: all 0.2s;
  box-shadow: 0 3px 10px rgba(143, 14, 32, 0.25);
}

.register-block a:hover {
  background: #a61228;
  transform: translateY(-1px);
}

.section-block {
  margin: 28px 0;
}

.section-block h3 {
  color: #8F0E20;
  font-size: 1.2rem;
  margin-bottom: 12px;
  padding-bottom: 6px;
  border-bottom: 2px solid #f0e0e3;
}

.section-block p {
  color: #444;
  font-size: 1.02rem;
  line-height: 1.8;
  text-align: justify;
  hyphens: auto;
  -webkit-hyphens: auto;
  -ms-hyphens: auto;
  word-break: break-word;
}

/* Mobile responsive */
@media (max-width: 600px) {
  .guest-hero {
    flex-direction: column;
    text-align: center;
    padding: 24px 16px;
    gap: 12px;
    max-width: 100%;
    border-radius: 12px;
  }

  .guest-hero .speaker-photo {
    width: 120px;
    height: 120px;
    border-width: 3px;
  }

  .guest-hero .speaker-info {
    min-width: unset;
  }

  .guest-hero .speaker-info h2 {
    font-size: 1.5rem;
  }

  .guest-hero .speaker-info .speaker-role {
    font-size: 1.05rem;
    text-align: center;
    line-height: 1.5;
  }

  .guest-hero .speaker-logos {
    justify-content: center;
    gap: 12px;
    margin-top: 4px;
  }

  .guest-hero .speaker-logos img {
    width: 55px;
    height: 55px;
    padding: 7px;
  }

  .talk-title-card {
    padding: 12px 0;
  }

  .talk-title-card h1 {
    font-size: 1.5rem;
    line-height: 1.4;
  }

  .talk-title-card .talk-subtitle {
    font-size: 1.05rem;
  }

  .event-card {
    flex-direction: column;
    gap: 4px;
    padding: 10px 16px;
    margin: 0;
    font-size: 0.88rem;
    align-items: flex-start;
  }

  .event-card .event-sep {
    display: none;
  }

  .register-block {
    flex-direction: column;
    text-align: center;
    padding: 8px 16px;
    gap: 6px;
  }

  .register-block p {
    font-size: 0.82rem;
  }

  .register-block a {
    padding: 6px 18px;
    font-size: 0.82rem;
  }

  .section-block {
    margin: 20px 0;
  }

  .section-block h3 {
    font-size: 1.05rem;
  }

  .section-block p {
    text-align: left;
    font-size: 0.92rem;
    line-height: 1.7;
  }
}
</style>

<div class="talk-title-card">
  <h1><span class="talk-type">Guest Lecture:</span> Multimodal AI for Human Understanding</h1>
  <p class="talk-subtitle">Decoding Emotion and Personality from Speech</p>
</div>

<div class="event-card">
  <span class="event-item"><span class="event-label">Date:</span> 24 June</span>
  <span class="event-sep">|</span>
  <span class="event-item"><span class="event-label">Time:</span> 2:00 &ndash; 3:00 PM</span>
  <span class="event-sep">|</span>
  <span class="event-item"><span class="event-label">Venue:</span> PGT Lab, Level 2, CS Building, Belfast</span>
  <span class="event-sep">|</span>
  <span class="event-item"><span class="event-label">Mode:</span> In-person + Online</span>
</div>
<div class="register-block">
  <p>If you want to attend in person or are not at Queen's, please register to attend.</p>
  <a href="https://forms.cloud.microsoft/e/kBPV0XB8R8" target="_blank">Register to Attend &rarr;</a>
</div>

<div class="guest-hero">
  <img src="{{ '/assets/imgs/hira.jpeg' | relative_url }}" alt="Dr. Hira Dhamyal" class="speaker-photo">
  <div class="speaker-info">
    <h2>Dr. Hira Dhamyal</h2>
    <div class="speaker-role">
      Machine Learning Engineer, Siri Team @ Apple<br>
      Ph.D. in Language Technologies, Carnegie Mellon University
    </div>
  </div>
  <div class="speaker-logos">
    <img src="{{ '/assets/imgs/apple.png' | relative_url }}" alt="Apple">
    <img src="{{ '/assets/imgs/cmu.png' | relative_url }}" alt="Carnegie Mellon University">
  </div>
</div>

<div class="section-block">
<h3>Abstract</h3>
<p>
When you speak, you reveal more than your words. The rhythm, tone, and texture of your voice encode psychological traits &mdash; your emotional state, your personality, even your behavioral tendencies.
</p>
<p>
In this talk, Dr. Dhamyal discusses building computational systems to decode two types of psychological traits from speech: <strong>emotion</strong> and <strong>personality</strong>. She introduces the use of <strong>CLAP</strong>, a contrastive audio-language model that uses natural-language descriptions of speech (rather than discrete category labels) to supervise emotion learning. This architecture allows the model to leverage the richness of natural language in addition to the speech signal. She then covers <strong>SELM</strong>, which extends this approach to address CLAP's limitations.
</p>
<p>
For personality, she revisits the classical <strong>OCEAN model</strong> &mdash; a 60-year-old psychological framework for human personality &mdash; by re-analyzing its basis labels using modern LLM-derived word representations, revealing interesting patterns in the data as looked at through the lens of large language models. She will also speak about her work utilizing contrastive audio-language models with acoustic prompts that achieve state-of-the-art zero-shot emotion recognition results.
</p>
<p>
In the last part of the talk, Dr. Dhamyal will briefly discuss her work on <strong>Siri at Apple</strong> and explore the future of speech processing in the age of foundational models. She will also reflect on her journey as a Ph.D. student at Carnegie Mellon and research internships at Microsoft and Meta, offering valuable advice and perspectives for students interested in pursuing careers in research and industry.
</p>
</div>

<div class="section-block">
<h3>About the Speaker</h3>
<p>
Dr. Dhamyal is a Machine Learning Engineer at Apple, in the Siri team. She received her Ph.D. in Language Technologies from Carnegie Mellon University's School of Computer Science in 2024, where she was a member of the Machine Learning for Signal Processing group and the Center for Voice Intelligence and Security.
</p>
<p>
Her research has focused on developing computational methods for decoding psychological traits from the human voice, utilizing contrastive audio-language models with acoustic prompts that achieve state-of-the-art zero-shot emotion recognition results. Her research has been applied in real-world settings, including voice forensics technology demonstrated live at the <strong>World Economic Forum</strong>.
</p>
<p>
She has publications in top conferences including <strong>ICASSP</strong>, <strong>Interspeech</strong>, <strong>EMNLP</strong>, and <strong>ACL</strong>, and has completed research internships at <strong>Microsoft</strong> and <strong>Meta</strong>.
</p>
</div>

<div class="section-block">
<h3>Readings</h3>
<p>TBC</p>
</div>
