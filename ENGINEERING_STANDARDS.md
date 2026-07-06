# Engineering Standards

Title: Engineering Standards
Version: 0.3.0
Status: Draft
Owner: AIG Engineering
Last Updated: 2026-07-06
Review Date: 2026-07-06
Approved By: AIG Engineering

## Repository Standards

Every repository should contain the following core documents:

- README.md
- ARCHITECTURE.md
- CONTRIBUTING.md
- SECURITY.md
- CHANGELOG.md
- LICENSE

## README Requirements

Every repository README should answer:

- Purpose
- Responsibilities
- Technology Stack
- Dependencies
- Running Locally
- Deployment
- Related Repositories

## Service Health Checks

Every service should expose health endpoints such as:

- /health/ready
- /health/live
- /version

## Logging Standard

Every log entry should include:

- Timestamp
- Service
- Environment
- Request ID
- Correlation ID
- User ID where appropriate
- Severity
- Message
