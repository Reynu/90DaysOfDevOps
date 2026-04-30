# Day 39 – What is CI/CD?

## Task 1: The Problem

### What can go wrong with 5 devs manually deploying?

* Two developers push conflicting code at the same time — one overwrites the other's changes (merge conflicts)

* A dev deploys untested code directly to production, breaking the live app

* No one knows who deployed what or when — debugging becomes a blame game

* One dev's environment has a different Python/Node version — works locally, crashes in prod

* No rollback plan — if the deploy breaks things, the team scrambles manually to fix it

### No rollback plan — if the deploy breaks things, the team scrambles manually to fix it

This happens when a developer's local environment differs from the server: different OS, different dependency versions, different env variables, different config files. CI/CD solves this by running code in a clean, controlled, identical environment every time — no "my machine" bias.

### How many times can a team safely deploy manually?

Realistically: 1–2 times a day, if they're disciplined. With CI/CD and automation: teams like Netflix and Amazon deploy hundreds of times per day. Manual deploys don't scale — CI/CD does.

