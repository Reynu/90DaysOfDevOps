# Day 46 – Reusable Workflows & Composite Actions

---

## ✅ Task 1: Concepts

### What is a reusable workflow?
A reusable workflow is a workflow that can be called by other workflows to avoid duplication.

### What is `workflow_call`?
A trigger that allows a workflow to be invoked by another workflow.

### Difference from normal action?
- Reusable workflow = full workflow (jobs, runners)
- Action = step-level reusable logic

### Where does it live?
.github/workflows/

---

## ⚙️ Task 2 & 3: Reusable Workflow + Caller

### Reusable Workflow
```yaml
# (paste reusable-build.yml)
