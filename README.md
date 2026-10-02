# Laravel Tasks — Junior Backend Roadmap (6 Months)

Training repo for a junior Laravel backend developer. Every task is a GitHub **issue**, grouped by **milestone** (one per phase) and labeled `phase-N`, `learning`, `deliverable` or `process`.

## Phase 1: Foundations (Weeks 1-4)
- Modern PHP 8.x: OOP, enums, traits, readonly, type hints
- Git workflow: branches, PRs, clean commits
- Laravel core: routing, controllers, Eloquent, migrations, seeders, Form Requests, API Resources
- **Deliverable:** CRUD REST API with validation and proper JSON responses

## Phase 2: Production-Grade APIs (Weeks 5-8)
- Auth with Sanctum, plus policies and gates
- Relationships, eager loading, and avoiding N+1
- Queues, jobs, events, notifications, file storage
- Centralized exception handling
- Testing with Pest or PHPUnit (feature tests)
- **Deliverable:** Auth-protected API with queued emails and 70%+ test coverage on core flows

## Phase 3: Architecture and Quality (Weeks 9-12)
- SOLID, Service/Action classes, DTOs, and when to use repositories (and when not to)
- Database: indexing, transactions, query optimization, `EXPLAIN`
- Redis caching
- Pint and Larastan/PHPStan in the workflow
- **Deliverable:** Refactor the Phase 2 project into a clean layered structure

## Phase 4: DevOps and Delivery (Months 4-5)
- Docker and Docker Compose
- CI/CD with GitHub Actions (tests, lint, deploy)
- Linux and Nginx basics, environment config
- Logging and monitoring (Sentry, Laravel Telescope or Pulse)
- API docs with OpenAPI or Scribe
- **Deliverable:** Dockerized app with an automated pipeline

## Phase 5: Advanced and Ownership (Month 6)
- Security: OWASP Top 10, rate limiting, mass-assignment, SQL injection and XSS prevention
- Third-party integrations: payment gateways, webhooks, idempotency
- Scalability: horizontal scaling, Horizon, database replicas
- **Deliverable:** Own a real feature end to end, from design to deployment

## Weekly Rhythm
- 1:1 with a mentor (30 min)
- One PR review given and one received
- A short written summary of what was learned (`docs/weekly/`, see `TEMPLATE.md`)

## How to Evaluate Progress
- **Code quality:** readable, tested, follows team conventions
- **Independence:** can estimate and deliver a ticket with little help
- **Debugging:** reads logs, reproduces issues, finds root causes
- **Communication:** clear PR descriptions and early blocker reporting

## Workflow
1. Pick the next open issue in the current milestone and assign it to yourself.
2. Every task issue already has its branch, named `feat/<issue-number>-short-name` (e.g. `feat/04-crud-rest-api`). It is written at the top of the issue.
3. Before starting, bring the branch up to date with `main`:
   ```bash
   git fetch origin
   git checkout feat/04-crud-rest-api
   git merge origin/main
   ```
4. Commit using [Conventional Commits](https://www.conventionalcommits.org/) (`feat: ...`, `fix: ...`, `test: ...`, `docs: ...`, `refactor: ...`).
5. Open a PR into `main` using the template, link the issue (`Closes #N`), request review.
6. Merge after approval; the issue closes automatically. Delete the branch after merge.

### Branch naming
| Type | Pattern | Example |
|---|---|---|
| Roadmap task / feature | `feat/<issue>-short-name` | `feat/05-sanctum-auth-policies` |
| Bug fix | `fix/<issue>-short-name` | `fix/31-task-404-json` |
| Weekly summary | `docs/weekly-YYYY-WW` | `docs/weekly-2026-41` |
