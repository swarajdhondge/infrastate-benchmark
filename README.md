# InfraState Benchmark

Companion repository for the paper **"Error Compounding in LLM-Based Infrastructure Simulation: A Multi-Domain Benchmark Study"** — Swaraj Dhondge, Independent Researcher.

A multi-domain benchmark measuring how well large language models track **infrastructure state** — Docker, Kubernetes, Terraform, Git, SQL, npm, Python — across multi-step command sequences, and how severely errors **compound** under auto-regressive evaluation. Ground truth is captured from real tool execution in sandboxed containers (no synthetic/LLM-generated labels).

**Highlights**
- First benchmark for LLM infrastructure state prediction: 1,496 entries · 80 scenarios · 7 domains + cross-domain.
- Evaluates 5 open models (7B–72B) under pure-LLM, hybrid deterministic-handler, and oracle conditions.
- Finds catastrophic error compounding: models retain only 13–24% of teacher-forced accuracy under auto-regressive deployment.

---

📄 **Preprint:** coming soon — the arXiv link will be posted here.

🔬 **Benchmark code + full reproduction instructions:** will be released here once the paper is posted.

✉️ **Contact:** Swaraj Dhondge · tosdhondge@gmail.com

---

> This repo is a landing page for now. Full dataset-generation and evaluation-harness instructions are held until the preprint is live.
