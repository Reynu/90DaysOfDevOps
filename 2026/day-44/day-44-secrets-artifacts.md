# Day 44 – Secrets, Artifacts & Running Real Tests in CI

---

## 🔐 Task 1: GitHub Secrets

### Setup
- Created secret: MY_SECRET_MESSAGE

### Observation
- Printing secret directly → shows `***`

### Why not print secrets?
- Logs are visible to users
- Secrets can leak → security risk
- GitHub masks them, but best practice is never print

---

## 🔑 Task 2: Secrets as Env Variables

- Passed secrets as environment variables
- Used safely without exposing values

---

## 📦 Task 3: Upload Artifacts

- Created file: report.txt
- Uploaded using `upload-artifact`

### Verification
- Downloaded from Actions tab successfully

---

## 🔄 Task 4: Artifact Sharing

- Job1 uploads file
- Job2 downloads and reads it

### Use Cases
- Sharing build outputs
- Passing logs/reports
- Multi-stage pipelines

---

## 🧪 Task 5: Real Tests in CI

- Ran Python script in CI
- Broke test → pipeline failed ❌
- Fixed test → pipeline passed ✅

---

## ⚡ Task 6: Caching

### What is cached?
- Dependencies (pip cache)

### Where is it stored?
- GitHub-managed storage

### Benefit
- Faster builds
- Reduced install time

---

## 🧠 Key Learnings

- Secrets must never be exposed
- Artifacts enable job-to-job data sharing
- CI pipelines validate real code
- Caching improves performance

---

## 📸 Screenshots

- Artifact download → (Add screenshot)
- Successful CI run → (Add screenshot)

---
