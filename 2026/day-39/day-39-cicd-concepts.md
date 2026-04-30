# Day 39 – What is CI/CD?

## Task 1: The Problem

### What can go wrong with 5 devs manually deploying?

* Two developers push conflicting code at the same time — one overwrites the other's changes (merge conflicts)

* A dev deploys untested code directly to production, breaking the live app

* No one knows who deployed what or when — debugging becomes a blame game

* One dev's environment has a different Python/Node version — works locally, crashes in prod

* No rollback plan — if the deploy breaks things, the team scrambles manually to fix it

