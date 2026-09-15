# Harness Bootstrapper

A cross-agent protocol for creating the five parts of an effective agent harness:

- context manager
- tool registry
- guardrails
- loop
- verifier

## Use it

Paste this into a coding agent that can read web pages:

> Read and follow https://raw.githubusercontent.com/bronsontaylor/harness-bootstrap/main/BOOTSTRAP.md

Run it from the project you want to equip. The agent will inspect the project, interview you in short batches, propose a harness contract for approval, build the infrastructure, verify it, and help you begin the first task.

The raw URL is the cross-agent entry point. `SKILL.md` also allows the repository to be packaged as a native agent skill where supported.

## What it creates

The protocol adapts to the project. It commonly creates project instructions plus a `.harness/` directory describing context, tools, guardrails, the operating loop, durable state, and verification. It does not presume a particular model, framework, or programming language.

## Safety

Approval of the proposed harness contract covers local, reversible repository work only. Deployment, spending money, sending messages, storing credentials, destructive operations, and production changes require explicit approval.

## Source

The five-part model is based on the formulation shown in the supplied reference images: **Agent Harness = Context Manager + Tool Registry + Guardrails + Loop + Verifier**.
