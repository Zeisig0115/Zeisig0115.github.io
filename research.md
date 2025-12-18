---
layout: page
permalink: /research/index.html
title: Research
---

<style>
/* 整体容器 */
.timeline-container {
border-left: 3px solid #e0e0e0;
margin-left: 1.5rem;
padding-left: 2rem;
position: relative;
}

/* 每个项目块 */
.timeline-item {
position: relative;
margin-bottom: 3.5rem;
}

/* 时间轴上的圆点 */
.timeline-marker {
position: absolute;
left: -2.6rem;
top: 0.2rem;
width: 16px;
height: 16px;
background: #fff;
border: 3px solid #005eb8; /* 你的主题色 */
border-radius: 50%;
z-index: 1;
}

/* 时间标签 */
.timeline-date {
font-size: 0.9rem;
font-weight: 700;
color: #555;
text-transform: uppercase;
margin-bottom: 0.5rem;
letter-spacing: 0.05em;
}

/* 项目标题 */
.project-title {
font-size: 1.3rem;
margin-top: 0;
margin-bottom: 0.5rem;
font-weight: 600;
}

.project-title a {
text-decoration: none;
color: #222;
}

/* 项目标签 (Badges) */
.tech-stack {
margin-bottom: 0.8rem;
}

.badge {
display: inline-block;
padding: 0.2rem 0.6rem;
margin-right: 0.5rem;
margin-bottom: 0.5rem;
background-color: #f0f0f0;
color: #333;
border-radius: 4px;
font-size: 0.75rem;
font-weight: 500;
}

/* 图片画廊容器 */
.project-gallery {
display: flex;
gap: 15px;
margin-top: 1rem;
overflow-x: auto;
}

/* 图片样式 */
.project-gallery img {
height: 140px;
width: auto;
border-radius: 5px;
box-shadow: 0 2px 5px rgba(0,0,0,0.1);
object-fit: cover;
transition: transform 0.2s;
}

.project-gallery img:hover {
transform: scale(1.05);
}

/* 引用块样式 */
.research-hook {
font-size: 1.1rem;
line-height: 1.6;
color: #444;
border-left: 4px solid #005eb8;
padding-left: 1rem;
margin-bottom: 3rem;
background: #f9f9f9;
padding: 1rem;
border-radius: 0 5px 5px 0;
}
</style>

<div class="research-hook">
"My research shifts from merely fitting models to actively guiding discovery. I develop structure-aware probabilistic methods that don't just learn from data, but efficiently decide what data to acquire next."
</div>

<div class="timeline-container">

<div class="timeline-item">
<div class="timeline-marker"></div>
<div class="timeline-date">2025 - Present (Phase III)</div>

<h3 class="project-title">Gaussian Processes for Implicit Functions & Phase Transitions</h3>
<div class="tech-stack">
<span class="badge">Bayesian Optimization</span>
<span class="badge">Physics-Informed ML</span>
<span class="badge">Uncertainty Quantification</span>
</div>

<p>
Addressing the challenge of non-smooth functions in scientific optimization. I developed a physics-informed GP to reconstruct latent system energy landscapes from constrained observations of stable states. By formally conditioning the GP posterior on observations of energy, zero-gradient, and curvature at equilibrium points, this method enables safe, active learning strategies that focus sampling on critical regions like phase transitions.
</p>

<div class="project-gallery">
<img src="/images/GP/energy_landscape.png" alt="Energy Landscape" onerror="this.style.display='none'">
<img src="/images/GP/structured_path.png" alt="Uncertainty Propagation" onerror="this.style.display='none'">
<img src="/images/GP/posterior.png" alt="Uncertainty Propagation" onerror="this.style.display='none'">
</div>
</div>

<div class="timeline-item">
<div class="timeline-marker"></div>
<div class="timeline-date">2025 - Present</div>

<h3 class="project-title">High-Throughput Microarray Bayesian Optimization</h3>
<div class="tech-stack">
<span class="badge">Combinatorial Optimization</span>
<span class="badge">Structure-Aware Design</span>
<span class="badge">Active Learning</span>
</div>

<p>
Designed a "Neighborhood-Augmented BO" for optimizing enzymatic reactions on adaptable microarray platforms. Introduced a slot-constrained encoding for mixed discrete-continuous variables to eliminate rejection sampling. The method leverages co-printed neighboring wells as low-cost local perturbations to accelerate surrogate learning and reduce regret without increasing the experimental budget.
</p>

<div class="project-gallery">
<img src="/images/microarray.png" alt="Microarray Platform" onerror="this.style.display='none'">
</div>
</div>

<div class="timeline-item">
<div class="timeline-marker"></div>
<div class="timeline-date">2025 - Present</div>

<h3 class="project-title">BO for Reactive Sputtering of Superconducting Thin Films</h3>
<div class="tech-stack">
<span class="badge">SAAS-Prior GP</span>
<span class="badge">High-Dimensional BO</span>
</div>

<p>
Improved calibration in high-dimensional materials synthesis. Benchmarked reactive sputtering meta-learning studies and fixed Gaussian Process Regression implementations that neglected inter-feature correlations. Replaced standard models with SAAS-prior GPs, demonstrating that Attentive Neural Processes (ANP) yield more reliable uncertainty estimates for downstream optimization compared to traditional methods.
</p>
</div>

<div class="timeline-item">
<div class="timeline-marker"></div>
<div class="timeline-date">2024 - 2025 (Phase II)</div>

<h3 class="project-title">Transformer-based Any-step Dynamics Model for Model-based RL</h3>
<div class="tech-stack">
<span class="badge">Model-Based RL</span>
<span class="badge">Transformers</span>
<span class="badge">Closed-Loop Control</span>
</div>

<p>
Moving from static data to sequential prediction. Proposed TADM to replace GRU encoders in dynamics modeling, enabling parallel training and reducing compounding errors in long-horizon rollouts. Achieved faster convergence and lower held-out NLL on Hopper-v5 benchmarks compared to ensemble baselines.
</p>

<div class="project-gallery">
<img src="/images/mbrl_transformer.png" alt="Transformer Attention" onerror="this.style.display='none'">
</div>
</div>

<div class="timeline-item">
<div class="timeline-marker"></div>
<div class="timeline-date">2024 - 2025</div>

<h3 class="project-title">Characterization of LNP Drug Delivery Vehicles by ML</h3>
<div class="tech-stack">
<span class="badge">Generative Modeling</span>
<span class="badge">Physics Simulation</span>
</div>

<p>
Addressed data scarcity by building a physics-informed small-angle X-ray scattering (SAXS) simulator. Synthesized high-fidelity scattering data from 3D morphologies to pretrain dual-task CNN/ResNet architectures. This created a scalable screening proxy that identifies dominant LNP types and estimates mixture fractions with 96% accuracy, reducing reliance on expensive cryo-EM imaging.
</p>
</div>

<div class="timeline-item">
<div class="timeline-marker"></div>
<div class="timeline-date">2022 - 2024 (Phase I)</div>

<h3 class="project-title">Structure-Aware ML for Hardware & Signals</h3>
<div class="tech-stack">
<span class="badge">Domain Adaptation</span>
<span class="badge">Neuromorphic Computing</span>
</div>

<p>
<strong>Perovskite Synaptic TFTs:</strong> Bridged device physics to learning rules by parameterizing ANN updates to match measured LTP/LTD conductance curves of CsFAMA transistors.<br><br>
<strong>NFC Device Identification:</strong> Developed a domain-adversarial pipeline to mitigate position-induced offsets in NFC signals, achieving robust cross-position generalization and eliminating handcrafted feature extraction.
</p>
</div>

</div>

<hr>
