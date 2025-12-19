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

.research-intro-block {
margin-bottom: 3rem;
padding: 1.5rem;
background-color: #f8f9fa;
border-radius: 8px;
border-left: 5px solid #005eb8;
}
.section-title {
margin-top: 0;
color: #333;
font-size: 1.5rem;
margin-bottom: 1rem;
}
.philosophy-list {
list-style-type: none;
padding-left: 0;
margin: 0;
}
.philosophy-list li {
margin-bottom: 1rem;
line-height: 1.5;
color: #444;
position: relative;
padding-left: 1.5rem;
}
.philosophy-list li::before {
content: "→";
position: absolute;
left: 0;
color: #005eb8;
font-weight: bold;
}
.philosophy-list strong {
color: #000;
font-weight: 600;
}


/* 新增：阶段分隔标题 */
.phase-header {
    position: relative;
    margin-top: 2rem;
    margin-bottom: 2rem;
    padding-left: 0; /* 对齐圆点 */
}

.phase-header h3 {
    margin: 0;
    font-size: 1.1rem;
    color: #005eb8; /* 使用您的主题色 */
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    background: #fff; /* 遮挡背景线，如果需要的话，或者保持透明 */
    display: inline-block;
    padding-right: 1rem;
}

/* 如果想让Phase标题也有个特殊的圆点 */
.phase-header::before {
    content: '';
    position: absolute;
    left: -2.9rem; /* 调整位置以对齐时间轴线 */
    top: 50%;
    transform: translateY(-50%);
    width: 24px;
    height: 4px; /* 横杠形状，或者用大圆点 */
    background: #005eb8;
}


</style>


<div class="research-intro-block">
<h2 class="section-title">Research Philosophy</h2>
<p>
My research journey is driven by a shift from <strong>merely fitting the existing data</strong> to <strong>strategically acquiring the information we need</strong>. This evolution consists of three key realizations:
</p>
<ul class="philosophy-list">
<li>
<strong>Structure as a Prior (Phase I):</strong> 
Early on, I realized standard ML fails to generalize in data-scarce settings. I addressed this by explicitly incorporating the system's intrinsic properties as <strong>structural inductive biases</strong>, ensuring model robustness and physical plausibility even in under-sampled regions.
</li>
<li>
<strong>Beyond Deterministic Metrics (Phase II):</strong>
I found performance gains can be spurious—often stemming from favorable artifacts of stochasticity. Shifting focus from "fitting data" to "knowing what we don't know," I prioritized <strong>calibrated uncertainty estimates</strong> over standard predictive metrics.
</li>
<li>
<strong>Active Decision Making (Phase III):</strong>
This led to my current focus on <strong>Structure-Aware Gaussian Processes & Bayesian Optimization</strong>. By combining structural priors with probabilistic surrogate modeling, I develop algorithms that leverage uncertainty to efficiently sample the input space and ultimately automate scientific discovery.
</li>
</ul>
</div>


<div class="timeline-container">

<div class="timeline-item phase-header" style="margin-bottom: 1.5rem;">
    <h3>Phase III: Active Decision Making</h3>
</div>

<div class="timeline-item">
<div class="timeline-marker"></div>
<div class="timeline-date">2025 - Present</div>

<h3 class="project-title">Gaussian Processes for Uncertainty Quantification of Implicit Functions</h3>
<div class="tech-stack">
<span class="badge">Gaussian Processes</span>
<span class="badge">Structure-Aware Prior</span>
<span class="badge">Uncertainty Quantification</span>
</div>

<div class="advisor-info" style="margin-top: 8px; margin-bottom: 8px; font-weight: 500; color: #555;">
<i class="fas fa-user-graduate"></i> Advisor: <a href="https://www.cs.cornell.edu/~bindel/" target="_blank" style="text-decoration: none; color: #0066cc;">Prof. David Bindel</a> (Cornell University)
</div>

<p>
Many scientific systems exhibit non-smooth responses that behave as implicit functions defined by equilibrium conditions. Rather than modeling the equilibria directly, we proposed reconstructing the underlying energy landscape with a structure-aware GP prior. By incorporating a semi-parametric mean function for energy regularization and conditioning on equilibrium constraints, this approach automatically recovers accurate, multi-modal posterior distributions, enabling safe active learning strategies that efficiently navigate phase transitions.
</p>

<div class="project-gallery">
<img src="/images/GP/energy_landscape.png" alt="Energy Landscape" onerror="this.style.display='none'">
<img src="/images/GP/structured_path.png" alt="structured_path" onerror="this.style.display='none'">
<img src="/images/GP/posterior.png" alt="posterior" onerror="this.style.display='none'">
<img src="/images/GP/empirical_dist.png" alt="empirical_dist" onerror="this.style.display='none'">
</div>
</div>



<div class="timeline-item">
<div class="timeline-marker"></div>
<div class="timeline-date">2025 - Present</div>

<h3 class="project-title">Adaptable Microarray Platform for High-Throughput Bayesian Optimization</h3>
<div class="tech-stack">
<span class="badge">Bayesian Optimization</span>
<span class="badge">Structure-Aware Prior</span>
<span class="badge">AI for Science</span>
</div>

<div class="advisor-info" style="margin-top: 8px; margin-bottom: 8px; font-weight: 500; color: #555;">
<i class="fas fa-user-graduate"></i> Advisor: <a href="https://ciralab.bme.cornell.edu/people.html" target="_blank" style="text-decoration: none; color: #0066cc;">Dr. Nate Cira</a> (Cornell University)
</div>

<p>
To optimize the enzymatic reaction TMB-HRP-H<sub>2</sub>O<sub>2</sub> with multiple additive reagents, we developed a high-throughput BO framework tailored for adaptable microarray platforms. Addressing a mixed discrete-continuous design space characterized by modal transitions and hardware-imposed cardinality constraints, we introduced a slot-based encoding that enforces feasibility by construction. This representation streamlines the optimization of acquisition functions while preserving the surrogate model's capacity to capture the system's inherent non-smooth structure.
</p>

<div class="project-gallery">
<img src="/images/BO1/loader.png" alt="Microarray Platform loader" onerror="this.style.display='none'">
<img src="/images/BO1/curves.png" alt="curves" onerror="this.style.display='none'">
<img src="/images/BO1/encoding.png" alt="encoding" onerror="this.style.display='none'">
</div>
</div>



<div class="timeline-item">
<div class="timeline-marker"></div>
<div class="timeline-date">2025 - Present</div>

<h3 class="project-title">Bayesian Optimization for Reactive Sputtering of Superconducting Thin Films</h3>
<div class="tech-stack">
<span class="badge">Gaussian Processes</span>
<span class="badge">Structure-Aware Prior</span>
<span class="badge">AI for Science</span>
</div>

<div class="advisor-info" style="margin-top: 8px; margin-bottom: 8px; font-weight: 500; color: #555;">
<i class="fas fa-user-graduate"></i> Advisor: <a href="https://jingjieyeo.github.io/about.html" target="_blank" style="text-decoration: none; color: #0066cc;">Dr. Jingjie Yeo</a> (Cornell University)
</div>

<p>
Improved calibration in high-dimensional materials synthesis. Benchmarked reactive sputtering meta-learning studies and fixed Gaussian Process Regression implementations that neglected inter-feature correlations. Replaced standard models with SAAS-prior GPs, demonstrating that Attentive Neural Processes (ANP) yield more reliable uncertainty estimates for downstream optimization compared to traditional methods.
</p>
</div>


<div class="timeline-item phase-header" style="margin-bottom: 1.5rem;">
    <h3>Phase II: Beyond Deterministic Metrics</h3>
</div>


<div class="timeline-item">
<div class="timeline-marker"></div>
<div class="timeline-date">2024 - 2025</div>

<h3 class="project-title">Transformer-based Any-step Dynamics Model for Model-based RL</h3>
<div class="tech-stack">
<span class="badge">Model-Based RL</span>
<span class="badge">Learning for Control</span>
</div>

<div class="advisor-info" style="margin-top: 8px; margin-bottom: 8px; font-weight: 500; color: #555;">
<i class="fas fa-user-graduate"></i> Course: <a href="https://www.cs.cornell.edu/courses/cs4756/2025sp/" target="_blank" style="text-decoration: none; color: #0066cc;">CS 5756</a> (Cornell University)
</div>

<p>
Revisiting Any-step Dynamics Models for MBRL. While reproducing an ICLR paper on Any-step Dynamics Model, I identified a discrepancy between the authors' reported error analysis and their appendix results. I hypothesized that the issue stemmed from the GRU encoder's inability to handle long-horizon dependencies effectively. I built a Transformer-based variant (TADM) that replaces the recurrent backbone with an attention mechanism. The resulting model not only corrected the error scaling behavior but also enabled parallel training , achieving state-of-the-art sample efficiency on MuJoCo benchmarks with significantly lower held-out NLL.
</p>

<div class="project-gallery">
<img src="/images/MBRL/structure.png" alt="structure" onerror="this.style.display='none'">
<img src="/images/MBRL/reward.png" alt="reward" onerror="this.style.display='none'">
<img src="/images/MBRL/error.png" alt="error" onerror="this.style.display='none'">
<img src="/images/MBRL/Hopper.gif" alt="Hopper" onerror="this.style.display='none'">
</div>
</div>



<div class="timeline-item">
<div class="timeline-marker"></div>
<div class="timeline-date">2024 - 2025</div>

<h3 class="project-title">Characterization of LNP Drug Delivery Vehicles by Machine Learning</h3>
<div class="tech-stack">
<span class="badge">AI for Science</span>
<span class="badge">Physics-based Simulation</span>
<span class="badge">Lipid Nanoparticle</span>
</div>

<div class="advisor-info" style="margin-top: 8px; margin-bottom: 8px; font-weight: 500; color: #555;">
<i class="fas fa-user-graduate"></i> Advisor: <a href="https://doerschuklab.bme.cornell.edu/people/" target="_blank" style="text-decoration: none; color: #0066cc;">Prof. Peter Doerschuk</a> (Cornell University)
</div>

<p>
Physics-Informed LNP Characterization via SAXS. To address the scarcity of realistic Small-Angle X-ray Scattering (SAXS) data for Lipid Nanoparticle (LNP) characterization, we constructed a physics-based simulator that synthesizes high-fidelity scattering profiles from cryo-EM morphologies using FFT approximations. By leveraging this synthetic data to pretrain dual-task deep learning architectures before fine-tuning on limited experimental measurements, we bridged the gap between theoretical physical laws and data-driven correlations. This sim-to-real framework achieved robust generalization (R<sup>2</sup> > 0.96) on held-out data, establishing a scalable computational proxy that significantly reduces reliance on expensive electron microscopy.
</p>

<div class="project-gallery">
<img src="/images/LNP/workflow.png" alt="workflow" onerror="this.style.display='none'">
<img src="/images/LNP/SAXS.png" alt="SAXS" onerror="this.style.display='none'">
<img src="/images/LNP/noise.png" alt="noise" onerror="this.style.display='none'">
<img src="/images/LNP/synthesis.png" alt="synthesis" onerror="this.style.display='none'">
<img src="/images/LNP/metrics.png" alt="metrics" onerror="this.style.display='none'">
</div>
</div>


<div class="timeline-item phase-header" style="margin-bottom: 1.5rem; margin-top: 4rem;">
    <h3>Phase I: Structure as a Prior</h3>
</div>


<div class="timeline-item">
<div class="timeline-marker"></div>
<div class="timeline-date">2023 - 2024</div>

<h3 class="project-title">NFC Device Identification Using Deep Learning and RF Fingerprinting</h3>
<div class="tech-stack">
<span class="badge">Metric Learning</span>
<span class="badge">Structure-aware Prior</span>
<span class="badge">RF Fingerprinting</span>
</div>

<div class="advisor-info" style="margin-top: 8px; margin-bottom: 8px; font-weight: 500; color: #555;">
<i class="fas fa-user-graduate"></i> Advisor: <a href="https://junqing-zhang.github.io/" target="_blank" style="text-decoration: none; color: #0066cc;">Prof. Junqing Zhang</a> (University of Liverpool)
</div>

<p>
Robust NFC Device Identification via Domain-Adversarial Learning. Standard RF fingerprinting often fails to generalize when reader-tag geometries change, primarily due to position-induced carrier-frequency offsets (CFO) and systematic signal distortions. Instead of treating these variations as random noise, we formulated the problem as a structured domain shift and developed a deep learning pipeline operating directly on raw baseband waveforms. By integrating multi-proxy metric learning strategies, our framework explicitly learns position-invariant representations, achieving 98.4% cross-configuration accuracy and mitigate the need for handcrafted feature extraction.
</p>

<div class="project-gallery">
<img src="/images/NFC/workflow.png" alt="workflow" onerror="this.style.display='none'">
<img src="/images/NFC/losses.png" alt="losses" onerror="this.style.display='none'">
<img src="/images/NFC/soft.png" alt="soft" onerror="this.style.display='none'">
<img src="/images/NFC/anomaly.png" alt="anomaly" onerror="this.style.display='none'">
<img src="/images/NFC/source.png" alt="source" onerror="this.style.display='none'">
<img src="/images/NFC/target.png" alt="target" onerror="this.style.display='none'">
</div>
</div>



<div class="timeline-item">
<div class="timeline-marker"></div>
<div class="timeline-date">2022 - 2023</div>

<h3 class="project-title">Perovskite-based Optoelectronic Artificial Synaptic TFT</h3>
<div class="tech-stack">
<span class="badge">Neuromorphic Computing</span>
<span class="badge">Physics-informed ML</span>
<span class="badge">Perovskite</span>
</div>

<div class="advisor-info" style="margin-top: 8px; margin-bottom: 8px; font-weight: 500; color: #555;">
<i class="fas fa-user-graduate"></i> Advisor: <a href="https://scholar.xjtlu.edu.cn/en/persons/ChunZhao/" target="_blank" style="text-decoration: none; color: #0066cc;">Prof. Chun Zhao</a> (Xi'an Jiaotong-Liverpool University)
</div>

<p>
Physics-Informed Learning for Perovskite-based Neuromorphic Systems. Treating emerging synaptic devices merely as noisy approximations of ideal weights often leads to unstable performance. To bridge the gap between device physics and learning dynamics, we characterized the potentiation-depression dynamics of CsFAMA perovskite TFTs and integrated these hardware constraints directly into the neural network's weight-update equations. We further enhanced this device-aware pipeline by incorporating influence-based relabeling strategies (RDIA-LS) to mitigate the effect of label noise. This co-design approach aligned learning dynamics with hardware behavior, demonstrating superior robustness under extreme noise regimes (up to 80%) and leading to a publication in <em>Nano Energy</em>.
</p>

<div class="project-gallery">
<img src="/images/TFT/workflow.png" alt="workflow" onerror="this.style.display='none'">
<img src="/images/TFT/device.png" alt="device" onerror="this.style.display='none'">
<img src="/images/TFT/covid.png" alt="covid" onerror="this.style.display='none'">
</div>
</div>

</div>

<hr>
