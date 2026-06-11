---
layout: talk
# title: "Agentic AI Seminar with AMD"
# lecture: "Guest"
# date: 2026-07-01
---

<style>
.talk-title-card {
  padding: 10px 0;
  margin: 8px 0 10px 0;
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
  width: 120px;
  height: 120px;
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

/* Tablet responsive */
@media (max-width: 900px) and (min-width: 601px) {
  .talk-title-card h1 {
    font-size: 1.7rem;
  }

  .talk-title-card .talk-subtitle {
    font-size: 1.1rem;
  }

  .guest-hero {
    padding: 16px 20px;
    gap: 16px;
  }

  .guest-hero .speaker-photo {
    width: 140px;
    height: 140px;
  }

  .guest-hero .speaker-info h2 {
    font-size: 1.6rem;
  }

  .guest-hero .speaker-info .speaker-role {
    font-size: 1.05rem;
    text-align: left;
  }

  .guest-hero .speaker-logos img {
    width: 95px;
    height: 95px;
    padding: 8px;
  }

  .event-card {
    font-size: 0.82rem;
    gap: 6px;
    padding: 12px 20px;
    flex-wrap: nowrap;
  }

  .register-block p {
    font-size: 0.95rem;
  }

  .register-block a {
    font-size: 0.95rem;
  }
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
    width: 80px;
    height: 80px;
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
  <h1><span class="talk-type">Seminar:</span> Agentic AI Design using AMD Technology</h1>
  <p class="talk-subtitle">with Hands-on Lab Powered by AMD Hardware</p>
</div>

<div class="event-card">
  <span class="event-item"><span class="event-label">Date:</span> 1 July</span>
  <span class="event-sep">|</span>
  <span class="event-item"><span class="event-label">Time:</span> TBC</span>
  <span class="event-sep">|</span>
  <span class="event-item"><span class="event-label">Venue:</span> PGT Lab, Level 2, CS Building, Belfast</span>
  <span class="event-sep">|</span>
  <span class="event-item"><span class="event-label">Mode:</span> In-person + Online</span>
</div>
<div class="register-block">
  <p>If you are not enrolled in the module, please register to attend the seminar.</p>
  <a href="#" target="_blank">Register for Seminar &rarr;</a>
</div>

<div class="guest-hero">
  <img src="{{ '/assets/imgs/mario.jpg' | relative_url }}" alt="Dr. Mario Ruiz" class="speaker-photo">
  <div class="speaker-info">
    <h2>Dr. Mario Ruiz</h2>
    <div class="speaker-role">
      Senior Member of Technical Staff, AMD University Program<br>
      Ph.D., Autonomous University of Madrid
    </div>
  </div>
  <div class="speaker-logos">
    <img src="{{ '/assets/imgs/amd.png' | relative_url }}" alt="AMD">
  </div>
</div>

<div class="section-block">
<h3>Abstract</h3>
<p>
Building trustworthy and capable agentic AI systems requires a foundation of open innovation, scalable compute, and transparent design principles. In this workshop, we explore how open-source initiatives &mdash; with AMD as a key driver &mdash; are accelerating the development of autonomous AI agents. We will highlight how AMD's latest Agent Computers, with integrated GPUs, provide optimized on-device compute for real-time inferencing and agentic workloads.
</p>
<p>
In the workshop, we will explore how we got from token generation to AI Agents. We will refresh the basics of context engineering and RAG systems. Then we will dive deeper into AI Agents and their fundamental components (model, orchestration and tools). Using the AUP Learning Cloud you will run hands-on labs to cement these concepts.
</p>
</div>

<div class="section-block">
<h3>What You'll Learn</h3>
<ul>
  <li>How token generation evolved into autonomous AI agents</li>
  <li>Context engineering and RAG system fundamentals</li>
  <li>Core components of AI agents: model, orchestration, and tools</li>
  <li>Hands-on experience building agents on the AUP Learning Cloud</li>
  <li>How AMD's Agent Computers enable on-device agentic workloads</li>
</ul>
</div>

<div class="section-block">
<h3>AMD Hardware</h3>
<p>
This seminar is powered by AMD's latest hardware provided to Queen's University Belfast. Participants will have access to:
</p>
<ul>
  <li><strong>AMD Agent Computers</strong> &mdash; Purpose-built PCs with integrated GPUs optimized for on-device AI inferencing and agentic workloads</li>
  <li><strong>AMD Ryzen AI Processors</strong> &mdash; Featuring dedicated NPUs for efficient local AI processing</li>
  <li><strong>AUP Learning Cloud</strong> &mdash; AMD University Program's cloud platform for hands-on labs and experimentation</li>
</ul>
</div>

<div class="section-block">
<h3>About the Speaker</h3>
<p>
Dr. Mario Ruiz is a Senior Member of Technical Staff in the AMD University Program, where he supports academics in adopting the latest AMD tools and technologies. He manages the Heterogeneous Accelerated Compute Cluster and brings over 10 years of experience designing high-performance FPGA and SoC implementations. For the past six years, he has worked closely with academics and researchers to maximize performance and efficiency with AMD and Xilinx technologies through direct support and training.
</p>
<p>
Before joining AMD, Mario earned his Ph.D. from the Autonomous University of Madrid, where his research focused on High-Level Synthesis for high-speed networking. His expertise spans electronics, digital design, and computer architecture, with a strong interest in heterogeneous accelerated computing.
</p>
</div>

<div class="section-block">
<h3>Preparation</h3>
<p>TBC</p>
</div>
