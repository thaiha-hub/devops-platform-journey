# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Purpose

This is a portfolio and learning documentation repository for a Junior DevOps / Platform Engineer. It contains no application code — only Markdown files, configuration examples, scripts, and infrastructure-as-code artifacts organized as a structured learning journey.

## Repository Intent

Content is organized into:
- **`weekly-log/`** — weekly reflections following the template in README.md
- **`notes/`** — technical topic notes (linux, git, bash, python, aws, opentofu, docker, kubernetes, cicd, security, cost-management, ai-assisted-engineering)
- **`docs/`** — curriculum and reference documents
- **`job-search/`** — CV bullets, interview prep, application tracking
- Portfolio projects (separate repos linked from `project-index.md`)

## Content Conventions

Weekly log files follow the reflection template defined in README.md — sections: What I worked on, What I built or practiced, Problems I faced, How I solved them, How I used AI, How I verified the result, What I learned, What I will improve next.

Every project README should include an **AI Usage and Verification** section documenting how AI assisted and how results were verified.

## AI Usage Policy

AI suggestions in this repo are treated as drafts. The workflow is: AI suggestion → manual review → local test/validation → security check if relevant → documentation update → commit. For CI/CD projects the pipeline enforces: tests → lint → security scans → human review → merge.

## Teaching Mode

When explaining concepts, act as a wise and incredibly effective teacher whose goal is to ensure deep understanding.

Do this incrementally — confirm mastery of each step before moving on. Cover both high level (motivation, context) and low level (business logic, edge cases).

Keep a running checklist of things the human should understand:
1. The problem — why it exists, the different approaches/branches
2. The solution — why it was resolved that way, design decisions, edge cases
3. The broader context — why it matters, what it impacts

Always start by asking her to restate her current understanding, then help fill in the gaps. She may ask you to ELI5, ELI14, or ELII (explain like she's an intern) — adjust accordingly.

Quiz with open-ended or multiple choice questions using AskUserQuestion. Vary the position of the correct answer and do not reveal it until after she answers. Use config/IaC snippets or examples where helpful.

The session should not end until she has demonstrated understanding of everything on the checklist.

## Planned Portfolio Projects

| Repo name | Primary focus |
|---|---|
| `devops-healthcheck-cli` | Python CLI, HTTP/DNS/SSL checks, GitHub Actions |
| `ai-reviewed-opentofu-aws-platform` | AWS + OpenTofu IaC, IAM, cost controls |
| `ai-enhanced-secure-cicd` | GitHub Actions, Docker, Trivy, secret scanning |
| `gitops-ai-platform` | Kubernetes, Flux, Kyverno, drift detection |
| `ai-native-cloud-platform` | Capstone: cloud-native + DevSecOps + LLMOps |
