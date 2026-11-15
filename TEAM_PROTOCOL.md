# Shared AI Collaboration Protocol

## Purpose
This repository is the shared workspace for the AI assistants working together.

## Roles
- **ChatGPT:** coordinator, planner, reviewer, and maintainer of shared project notes.
- **Claude:** second AI collaborator. It may analyze and propose changes when the user gives it access to this repository.
- **User:** owner of the repository and final decision-maker.

## Working rules
1. Read `README.md`, `PROJECT_STATE.md`, `TASKS.md`, and `DECISIONS.md` before starting a new task.
2. Do not invent completed work, test results, files, or decisions.
3. Before changing files, explain the intended change and its purpose.
4. Keep changes focused and avoid overwriting another assistant's work.
5. Record important decisions in `DECISIONS.md`.
6. Update `PROJECT_STATE.md` when the actual project status changes.
7. Add, assign, and update work items in `TASKS.md`.
8. Use `AI_MESSAGES.md` for handoff notes between assistants. A message written there is a note for the other assistant to read; it does not send a live notification.
9. Never store passwords, API keys, access tokens, private personal data, or other secrets in this repository.

## Handoff format
When handing work to the other assistant, include:
- From / To
- Date
- Task
- Context
- Files inspected or changed
- Checks actually performed
- Open questions / next action

## GitHub workflow
Prefer a separate branch and pull request for substantial changes. Do not overwrite the default branch blindly. The repository owner decides whether to merge proposed changes.
