# Product backlog and labels

This repository tracks user stories for the GiftLink capstone project using GitHub issue labels. Use these labels when creating issues from the `User Story` template.

## Labels

| Label | Color | Purpose |
| --- | --- | --- |
| `new` | `#1f883d` | Newly created stories that still need triage. *(Default label on the user-story template.)* |
| `backlog` | `#0969da` | Stories selected for the current sprint. |
| `icebox` | `#6e7781` | Lower-priority stories to be scheduled later. |
| `technical debt` | `#fbca04` | Work that reduces debt or enables future delivery. |

## User stories and triage

All stories are created with the `new` label, then triaged so that each has exactly one of `backlog` or `icebox` applied. The following stories are prepared with brief acceptance criteria to be sprint-ready.

### Backlog (planned now)

1. **Finish user stories** — Story descriptions and acceptance criteria are complete for the sprint (`backlog`).
2. **Initialize and populate MongoDB** — Database is provisioned with seed data accessible via the API (`backlog`).
3. **Run skeleton application** — Backend and frontend start successfully with environment configuration (`backlog`).
4. **Implement a landing page and navigation** — Landing page shows brand messaging and links to core flows (`backlog`).
5. **Add authentication components and logic** — Users can sign up, sign in, and see protected routes after login (`backlog`).
6. **Research authentication in React and Express** — Investigation results documented for the team (`backlog`, `technical debt`).

### Icebox (deferred)

7. **Implement Gifts details page** — View renders gift data with imagery and metadata (`icebox`).
8. **Implement a search component** — Users can search gifts with debounced queries (`icebox`).
9. **Design and implement the comments feature** — Authenticated users can add and view comments per gift (`icebox`).
10. **Containerize the services and applications** — Docker images build and run for backend and frontend (`icebox`).
11. **Deploy backend and frontend** — Services deployed to target environment with health checks (`icebox`).
