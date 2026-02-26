# GiftLink product backlog and labels

This repository tracks the GiftLink capstone backlog and label plan that should be mirrored in GitHub issues.

## Labels
- **new** (e.g., `#1e90ff`): freshly captured stories awaiting triage.
- **backlog** (e.g., `#228b22`): prioritized stories for the current sprint.
- **icebox** (e.g., `#708090`): deprioritized stories for later sprints.
- **technical debt** (yellow, `#ffd700`): engineering tasks that reduce debt without direct user-facing value.

All stories start with the `new` label and are triaged into exactly one of the other labels. The `technical debt` label can accompany a story when applicable.

## User stories created from the template
Each story uses the existing `User Story` issue template with filled details and acceptance criteria.

### Backlog (current sprint)
1. **Finish user stories** — As a product owner, I need completed user-story issues so that the team has a ready backlog.  
   **Acceptance:** All ten stories exist with completed fields and labels.
2. **Initialize and populate MongoDB** — As a developer, I need seeded MongoDB data so that services can run locally.  
   **Acceptance:** MongoDB container boots with sample gift data loaded.
3. **Run skeleton application** — As a developer, I need the baseline services running so that integration can proceed.  
   **Acceptance:** Backend and frontend start locally with health/status endpoints responding.
4. **Implement a landing page and navigation** — As a shopper, I need an entry point and nav so that I can explore gifts.  
   **Acceptance:** Landing page renders hero, navigation links, and routes correctly.
5. **Add authentication components and logic** — As a user, I need to sign up/sign in so that my preferences persist.  
   **Acceptance:** Auth views exist, tokens are stored client-side, and protected routes enforce auth.

### Icebox (later sprints)
6. **Implement gift details page** — As a user, I need a detailed view of a gift so that I can decide to purchase or save it.  
   **Acceptance:** Details page shows description, price, and related items.
7. **Implement a search component** — As a user, I need to search for gifts so that I can find items quickly.  
   **Acceptance:** Search input returns filtered results against the catalog.
8. **Design and implement the comments feature** — As a user, I need to leave feedback so that others see reviews.  
   **Acceptance:** Users can post, edit, and view comments tied to gifts.
9. **Containerize the services and applications** — As an engineer, I need Docker images so that deployments are consistent.  
   **Acceptance:** Backend and frontend build into runnable images with documented commands.
10. **Deploy backend and frontend** — As a product owner, I need live environments so that stakeholders can test.  
    **Acceptance:** Services are deployed with accessible URLs and basic uptime checks.

### Technical debt
- **Research authentication in React and Express** — Investigate best practices for secure auth flows to reduce future refactors.  
  **Labels:** `technical debt` (applies alongside status label if scheduled).
