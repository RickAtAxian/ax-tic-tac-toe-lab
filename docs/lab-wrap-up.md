# Lab Wrap-Up

## Handoff References

- Repository: `https://github.com/RickAtAxian/ax-tic-tac-toe-lab.git`
- Web app: `http://rickw-ai-tic-tac-toe-lab.s3-website-us-west-2.amazonaws.com`
- Server: `http://ec2-34-217-60-117.us-west-2.compute.amazonaws.com:8787`

## Project Docs

- [README.md](/workspaces/ai-tic-tac-toe-lab/README.md)
- [AGENTS.md](/workspaces/ai-tic-tac-toe-lab/AGENTS.md)
- [WorkTracker.md](/workspaces/ai-tic-tac-toe-lab/WorkTracker.md)
- [LD-WorkLog.md](/workspaces/ai-tic-tac-toe-lab/LD-WorkLog.md)
- [architecture.md](/workspaces/ai-tic-tac-toe-lab/docs/architecture.md)
- [multiplayer-architecture.md](/workspaces/ai-tic-tac-toe-lab/docs/multiplayer-architecture.md)
- [project-organization.md](/workspaces/ai-tic-tac-toe-lab/docs/project-organization.md)
- [infra/README.md](/workspaces/ai-tic-tac-toe-lab/infra/README.md)

## User Stories Given to AI

- [Phase 1 user stories](/workspaces/ai-tic-tac-toe-lab/phases/phase-1/phase-1.md)
- [Phase 2 user stories](/workspaces/ai-tic-tac-toe-lab/phases/phase-2/phase-2.md)
- [Phase 3 user stories](/workspaces/ai-tic-tac-toe-lab/phases/phase-3/phase-3.md)
- [Execution tracker](/workspaces/ai-tic-tac-toe-lab/WorkTracker.md)

## Build And Test Commands

- [Available Scripts](/workspaces/ai-tic-tac-toe-lab/README.md#available-scripts)
- [Testing](/workspaces/ai-tic-tac-toe-lab/README.md#testing)
- [Phase 3 Review Commands](/workspaces/ai-tic-tac-toe-lab/README.md#phase-3-review-commands)

Core commands:

- `npm install`
- `npm run build`
- `npm run test:unit`
- `npm run test:server`
- `npm run test:e2e`
- `npm run coverage`
- `npm run package:server`

## Recommendations For The Lab

- Keep the repo phase-driven with explicit review gates after meaningful milestones.
- Make the tracker and work log part of the required process, not optional docs.
- Require one canonical requirements file per phase plus visual references when UI behavior matters.
- Prefer terminal-first commands for build, test, coverage, packaging, and deployment so AI and humans share the same execution surface.
- Use a shared-contract layer early when the lab moves from client-only work to server-backed work.
- Keep deployment infrastructure intentionally low-cost and simple so the lab focuses on AI-assisted delivery rather than cloud complexity.

## Context Management Notes

- The main context anchors were `AGENTS.md`, the phase requirement docs, `WorkTracker.md`, and `LD-WorkLog.md`.
- `AGENTS.md` held durable repo rules and lessons so repeated mistakes did not need to be rediscovered.
- `WorkTracker.md` constrained scope to one accepted story at a time and preserved milestone state.
- `LD-WorkLog.md` captured implementation decisions, corrections, commands, and verification so the project could grow without relying on ephemeral chat context.
- Architecture and organization docs were updated as the codebase evolved so later work could read the repo instead of re-deriving structure from scratch.

## Work Style Changes Across Larger Bodies Of Work

- Early work was more exploratory: establish structure, verify assumptions, and keep changes narrow.
- As the repo grew, dispatch became more milestone-oriented: define one story, implement only that slice, verify it, stop for review, then checkpoint it.
- For larger volumes of work, the style shifted from describing individual edits to maintaining stable operating documents and relying on those as shared memory.
- Receiving larger requirements worked better when ambiguous terms were normalized against the actual UI and codebase before implementation.

## Codex CLI Learnings

- Codex CLI worked best when paired with strong local repo documents that acted as durable memory between turns.
- It was important to keep commands scriptable and terminal-first because that gave Codex a clean verification path.
- Small, reviewable commits after accepted milestones reduced risk and made recovery straightforward.
- Documentation discipline mattered more as the project scaled; without repo-native context documents, the cost of reloading state would have been much higher.
- Deployment work exposed real operational gaps quickly, such as CORS assumptions, production API origin wiring, and script output that needed to be machine-readable.
