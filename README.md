# AI Docs

Title: AI Docs
Version: 0.3.0
Status: Draft
Owner: AIG Engineering
Last Updated: 2026-07-06
Review Date: 2026-07-06
Approved By: AIG Engineering

This repository contains the core documentation for the AIG Platform and North Star ecosystem.

## Repository Role

This repository defines what is being built and why. The implementation and engineering assets live in the separate platform repository.

## Related Repository

- [aig-platform](https://github.com/AIG-Global/aig-platform)

## Structure

- Governance: [00-governance](00-governance/README.md)
- Architecture: [01-architecture](01-architecture/README.md)
- Product: [02-product](02-product/README.md)
- Security: [03-security](03-security/README.md)
- Engineering: [04-engineering](04-engineering/README.md)
- Operations: [05-operations](05-operations/README.md)
- Sprints: [06-sprints](06-sprints/README.md)
- ADRs: [adr](adr/README.md)
- Diagrams: [diagrams](diagrams/README.md)
- Templates: [templates](templates/README.md)

## Key Documents

- [ARCHITECTURE.md](ARCHITECTURE.md)
- [DECISIONS.md](DECISIONS.md)
- [ENGINEERING_STANDARDS.md](ENGINEERING_STANDARDS.md)

## Engineering Standards

This repository now documents the shared engineering expectations for all repositories:

- Core repository files: README, ARCHITECTURE, CONTRIBUTING, SECURITY, CHANGELOG, LICENSE
- README expectations: purpose, responsibilities, technology stack, dependencies, local run steps, deployment, and related repositories
- Health checks: /health/ready, /health/live, /version
- Logging: timestamp, service, environment, request ID, correlation ID, user ID where appropriate, severity, and message
