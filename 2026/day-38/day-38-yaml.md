

# Day 38 – YAML Basics

# Task 1 & 2: person.yaml

name: Renu
role: DevOps Engineer
experience_years: 4+
learning: True #Boolean
tools:
  - Linux
  - Docker
  - Shell Scripting
  - Git & Github
  - GitHub Actions
  - Kubernetes
  - Terraform

hobbies: ["Automation", "cricket", "music"]
# Task 3 & 4: server.yaml

server:
  name: MyServer
  ip: "127.0.0.1"
  port: 80

database:
  host: localhost
  name: local_db
  credentials:
    user: admin
    password: password123

startup_script: |
  #!/bin/bash
  echo "Starting server..."
  systemctl status nginx
  # Add your startup commands here

start_script: >
  #!/bin/bash
  echo "Starting server..."
  systemctl status nginx
  # Add your startup commands here
Notes

Two ways to write a list in YAML

Block style (one item per line):

tools:
  - Docker
  - Kubernetes
Inline style (comma-separated in brackets):

hobbies: ["Automation", "cricket", "music"]
| vs > — When to use which?

Style	Behavior	Use When
| (literal)	Preserves newlines	Shell scripts, code, config files — line breaks matter
> (folded)	Folds newlines into spaces	Long descriptions or messages — readability only
Task 5: Validate YAML

# Install
pip install yamllint

# Validate
yamllint server.yaml
yamllint person.yaml

# Intentional break (add a tab) gives:
# Error: found character '\t' that cannot start any token
Task 6: Spot the Difference

# Block 1 - correct
name: devops
tools:
  - docker
  - kubernetes
# Block 2 - broken
name: devops
tools:
- docker
  - kubernetes
What's wrong with Block 2:

- docker is not indented under tools: — it should be 2 spaces in
- kubernetes is indented more than - docker, making it look like a nested child instead of a sibling list item
Both list items must be at the same indentation level under tools:
3 Key Learnings

Indentation is everything — YAML uses spaces only (never tabs). 2 spaces is standard. Wrong indentation = broken file.
Types matter without quotes — true is a boolean, "true" is a string. 80 is an integer, "80" is a string. Be intentional.
Two multi-line styles for different needs — Use | when newlines are meaningful (scripts/code), use > when you just want clean readable YAML but the content is one logical string.

