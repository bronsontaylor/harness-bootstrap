# Harness Bootstrapper

A cross-agent protocol for creating the five parts of an effective agent harness:

- context manager
- tool registry
- guardrails
- loop
- verifier

## Use it

Open Codex, Claude Code, Cursor, or another coding agent that can read web pages, then paste:

> Read and follow https://raw.githubusercontent.com/bronsontaylor/harness-bootstrap/main/BOOTSTRAP.md

You can use it in any of three situations:

1. **Start with an idea:** open the agent in the parent directory where you want the new project created. Tell it your idea after the URL. It will interview you, recommend undecided technical choices, create the project and harness, verify them, and guide the first task.
2. **Equip an existing project:** open the agent inside that project's directory. It will inspect what is already there before interviewing you and will preserve existing conventions.
3. **Build a standalone harness:** tell the agent that the workflow spans projects or is not attached to an application. It will establish a dedicated workspace and design around the workflow's inputs and outputs.

### Starting a new project

```text
Read and follow https://raw.githubusercontent.com/bronsontaylor/harness-bootstrap/main/BOOTSTRAP.md

I want to create a service that watches a support inbox, drafts answers from our
documentation, and sends nothing until a person approves it. I have not created
the project yet, and I would like you to recommend the stack.
```

### Equipping an existing project

```text
Read and follow https://raw.githubusercontent.com/bronsontaylor/harness-bootstrap/main/BOOTSTRAP.md

I want a harness that can investigate bug reports in this application, implement
fixes, run its checks, and prepare changes for human review.
```

The raw URL is the cross-agent entry point. `SKILL.md` also allows the repository to be packaged as a native agent skill where supported.

## What it creates

The protocol adapts to the starting point. For a new idea, it can create the project workspace and agreed starter architecture as well as the harness. For existing work, it commonly adds project instructions plus a `.harness/` directory describing context, tools, guardrails, the operating loop, durable state, and verification. It does not presume a particular model, framework, or programming language.

## Safety

Approval of the proposed harness contract covers local, reversible repository work only. Deployment, spending money, sending messages, storing credentials, destructive operations, and production changes require explicit approval.

## Source

The five-part model is based on the formulation shown in the supplied reference images: **Agent Harness = Context Manager + Tool Registry + Guardrails + Loop + Verifier**.
