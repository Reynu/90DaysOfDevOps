# Day 42 – Runners: GitHub-Hosted & Self-Hosted

---

## ✅ Task 1: GitHub-Hosted Runners

### Workflow
- Ran jobs on:
  - ubuntu-latest
  - windows-latest
  - macos-latest

### Output Observed
- OS name printed
- Hostname printed
- Current user printed

### Notes
**What is a GitHub-hosted runner?**  
A GitHub-hosted runner is a virtual machine provided and managed by GitHub to execute workflows.

**Who manages it?**  
GitHub manages provisioning, updates, and maintenance.

---

## 🔍 Task 2: Pre-installed Tools

### Tools Checked
- Docker
- Python
- Node
- Git

### Observation
All tools were already installed and ready to use.

### Notes
Pre-installed tools:
- Reduce setup time
- Speed up CI pipelines
- Avoid dependency installation overhead

---

## 🖥️ Task 3: Self-Hosted Runner Setup

### Steps Performed
- Navigated to: Repo → Settings → Actions → Runners
- Added new self-hosted runner (Linux)
- Ran setup commands on local machine / VM
- Started runner using:
  ```bash
  ./run.sh
