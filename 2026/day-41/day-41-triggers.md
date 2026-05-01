# Day 41 – Triggers & Matrix Builds

---

## ✅ Task 1: Pull Request Trigger

### Workflow
```yaml
# .github/workflows/pr-check.yml
name: PR Check

on:
  pull_request:
    branches: [main]
    types: [opened, synchronize]

jobs:
  pr-check:
    runs-on: ubuntu-latest
    steps:
      - run: echo "PR check running for branch: ${{ github.head_ref }}"
