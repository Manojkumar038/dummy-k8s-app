# Digital Banking Platform (Synthetic Engineering Demo)

A deliberately synthetic application repository used to exercise Jira-to-GitHub traceability and an Engineering Intelligence analysis agent. This is **not** a real banking system and must not be used for real financial activity.

## Project scope

- Authentication and security (F1): registration, login, password reset, MFA, session expiry.
- Account and beneficiary management (F2): account overview, transaction history, profile updates, beneficiary verification.
- Payments, transfers and notifications (F3): simulated UPI, IMPS, NEFT and RTGS flows, receipts and transaction alerts.

## Technology target

- Backend: Java 21, Spring Boot, Maven
- Frontend: React
- Data: PostgreSQL
- CI: GitHub Actions
- Container target: Docker; deployment events are simulated unless explicitly configured.

The current repository intentionally uses **dummy files and metadata**, not a production banking implementation.

## Jira and Git conventions

- Epic: EPIC-100
- Features: F1, F2, F3
- User stories: US101–US118
- Branches: `feature/F1-auth-security`, `feature/F2-account-beneficiaries`, `feature/F3-payments-notifications`
- Story branches: `story/us101` etc.
- Commit messages: `[US101] Add synthetic registration fixture` or `[F1] Update authentication test data`
- PR titles and bodies should reference the corresponding Jira story IDs.

## Repository layout

```
backend/                 # synthetic Spring Boot project fixtures
frontend/                # synthetic React project fixtures
database/                # PostgreSQL schema fixtures
docs/                    # project, Jira and simulation documentation
tests/                   # synthetic test fixtures
.github/workflows/       # lightweight validation workflows
```

## Historical-data integrity

Backdated Git commit author/committer dates can be used for **synthetic commit history**. GitHub PR creation, review, Actions run and deployment timestamps are platform-generated events and cannot honestly be backdated through normal GitHub operations. Any simulated historical PR/review/deployment records must be stored separately and explicitly labelled `synthetic`; actual GitHub events must be labelled `actual`.

## Safety

- No real credentials, customer data, bank account details, payment rails or external banking integrations.
- Payment examples are fixtures only.
- Never add secrets to this public repository.
- Use GitHub Actions only for harmless validation tasks.
