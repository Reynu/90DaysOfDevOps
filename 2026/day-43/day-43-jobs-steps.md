# Day 43 – Jobs, Steps, Env Vars & Conditionals

---

## ✅ Task 1: Multi-Job Workflow

### Workflow
- Created 3 jobs: build → test → deploy
- Used `needs:` to define dependencies

### Key Concept
- `needs:` ensures job execution order

---

## 🌍 Task 2: Environment Variables

### Levels Used
- Workflow level → APP_NAME
- Job level → ENVIRONMENT
- Step level → VERSION

### GitHub Context Used
- Commit SHA → $GITHUB_SHA
- Actor → $GITHUB_ACTOR

---

## 🔁 Task 3: Job Outputs

### Flow
- First job sets output (date)
- Second job consumes it

### Key Concept
- Outputs allow sharing data between jobs

### Why use outputs?
- Pass dynamic values (version, artifact path)
- Enable dependent job logic
- Avoid recomputation

---

## ⚙️ Task 4: Conditionals

### Implemented:
- Run step only on main branch
- Run step on failure
- Run job only on push
- Used `continue-on-error`

### Observation:
- `continue-on-error: true` allows workflow to continue even if step fails

---

## 🚀 Task 5: Smart Pipeline

### Flow:
- lint + test run in parallel
- summary runs after both

### Features:
- Branch detection
- Commit message logging

---

## 🧠 Key Concepts

### `needs:`
Defines dependency between jobs and ensures execution order.

### `outputs:`
Allows passing data from one job to another.

---

## 📸 Screenshots

(Add workflow graph and execution screenshots)

---
