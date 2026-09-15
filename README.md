# Harness Bootstrapper

A cross-agent protocol that starts with a person's goal and creates the five parts of an effective agent harness:

- context manager
- tool registry
- guardrails
- loop
- verifier

## Use it

Open Codex, Claude Code, Cursor, or another coding agent that can read web pages, then paste:

> Read and follow https://raw.githubusercontent.com/bronsontaylor/harness-bootstrap/main/BOOTSTRAP.md

The user does not need to understand harness terminology or answer a technical questionnaire. The agent decides what to ask as the conversation develops, using the five parts as its internal design model.

If the user pastes only the URL, the agent begins with:

> What would you like to make possible?

This does not assume that a project already exists. The user can answer with a rough idea, a problem, a wish, or something they have already started.

You can use it in any of three situations:

1. **Start with an idea:** open the agent in the parent directory where you want the new project created. Tell it your idea after the URL in your own words. It will ask only the questions that become useful, recommend undecided technical choices, create the project and harness, verify them, and guide the first task.
2. **Equip an existing project:** open the agent inside that project's directory. It will inspect what is already there before interviewing you and will preserve existing conventions.
3. **Build a standalone harness:** tell the agent that the workflow spans projects or is not attached to an application. It will establish a dedicated workspace and design around the workflow's inputs and outputs.

### Starting a new project

```text
Read and follow https://raw.githubusercontent.com/bronsontaylor/harness-bootstrap/main/BOOTSTRAP.md

I run a small charity and answering the same email questions takes too much time.
I would like something that helps with that, but people should stay in control.
I have not created anything yet.
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
