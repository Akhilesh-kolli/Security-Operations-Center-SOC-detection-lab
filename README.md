# Cymarl-Framework

<p align="center">
  <img src="https://img.shields.io/badge/SIEM-Splunk-blue">
  <img src="https://img.shields.io/badge/Endpoint-Sysmon-brightgreen">
  <img src="https://img.shields.io/badge/Attack-Simulation-orange">
  <img src="https://img.shields.io/badge/Kali-Linux-red">
  <img src="https://img.shields.io/badge/Logs-Windows_Event_Logs-yellow">
  <img src="https://img.shields.io/badge/MARL-PPO-purple">
  <img src="https://img.shields.io/badge/Framework-Cybersecurity-darkblue">
</p>

---

# Cybersecurity Multi-Agent Reinforcement Learning Framework

Cymarl-Framework is a cybersecurity-focused Multi-Agent Reinforcement Learning (MARL) framework developed for attacker–defender simulations in enterprise-like network environments.

The project models adversarial cyber interactions where intelligent attacker and defender agents learn dynamically using Proximal Policy Optimization (PPO). The framework enables attack simulation, defense strategy evaluation, reward optimization, training visualization, and cyber risk experimentation.

---

# Key Features

- Multi-Agent Reinforcement Learning (MARL)
- PPO-based attacker–defender training
- Cyber attack simulation environment
- Dynamic reward engineering
- Network intrusion experimentation
- Security event simulation
- Training metrics and visualization
- GIF-based simulation rendering
- Research-oriented cyber environment
- Attack path and defense strategy analysis

---

# Technologies Used

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Reinforcement Learning | PPO |
| Visualization | Matplotlib |
| Data Processing | NumPy, Pandas |
| Cybersecurity Monitoring | Splunk |
| Endpoint Monitoring | Sysmon |
| Operating Environment | Kali Linux |
| Logging | Windows Event Logs |

---

# Project Workflow

```text
Attacker Agent
       ↓
Cyber Environment Simulation
       ↓
Defender Agent
       ↓
Reward Calculation
       ↓
PPO Policy Optimization
       ↓
Training Metrics & Visualization
```

---

# Project Structure

```text
Cymarl-Framework/
│
├── src/
├── models/
├── logs/
├── plots/
├── gifs/
├── reports/
├── compute_metrics.py
├── generate_gif.py
├── plot_training.py
├── requirements.txt
└── README.md
```

---

# Installation

Clone repository:

```bash
git clone https://github.com/Akhilesh-kolli/Cymarl-Framework-.git
```

Move into project folder:

```bash
cd Cymarl-Framework-
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# Running the Framework

Run PPO training:

```bash
python train.py
```

Generate metrics:

```bash
python compute_metrics.py
```

Plot training graphs:

```bash
python plot_training.py
```

Generate simulation GIF:

```bash
python generate_gif.py
```

---

# Generated Outputs

The framework produces:

- PPO training logs
- Reward convergence graphs
- Success-rate analysis
- Attack efficiency metrics
- Defender response metrics
- Cyber simulation visualizations
- Animated GIF simulations

---

# Research Applications

- AI-driven cybersecurity research
- Autonomous cyber defense simulation
- Attacker–defender RL experimentation
- Cyber threat modeling
- Reinforcement learning security analysis
- Adaptive defense strategy evaluation

---

# Future Enhancements

- Real-time IDS/IPS integration
- Distributed MARL training
- Advanced adversarial learning
- SOC integration support
- Explainable AI for cyber defense
- Live network traffic simulation

---

# Author

## Akhilesh Kolli

Cybersecurity Research | Reinforcement Learning | Threat Simulation

GitHub:
https://github.com/Akhilesh-kolli

---

# License

This project is intended for academic, educational, and cybersecurity research purposes.
