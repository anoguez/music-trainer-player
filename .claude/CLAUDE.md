# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

**music-trainer-player** — a music training and playback application. The repository is currently in its initial setup phase with no source code committed yet.

## Tech Stack

- **Framework:** React Router v7
- **Styling:** Tailwind CSS
- **Language:** TypeScript
- **Runtime:** Node.js

## Agent Roles

This project uses a multi-agent setup defined in [.claude/agent-capacity.json](.claude/agent-capacity.json). Each role maps to a specialized subagent with a max concurrency of 1:

| Role | Agent | GitHub Label |
|------|-------|--------------|
| `backend` | `backend-api-developer` | `agent:backend` |
| `frontend` | `senior-frontend` | `agent:frontend` |
| `devops` | `devops-engineer` | `agent:devops` |
| `qa` | `qa-test-engineer` | `agent:qa` |
| `architect` | `software-architect` | `agent:architect` |
| `writer` | `technical-writer` | `agent:writer` |

When dispatching work via `/orchestrate` or `/plan`, use these role labels to route tasks to the correct specialist agent.
