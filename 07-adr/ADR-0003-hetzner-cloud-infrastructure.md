# ADR-0003 — Hetzner Cloud Infrastructure

Version: 1.0.0
Status: Accepted
Owner: AIG Engineering
Last Updated: 2026-07-06
Review Date: 2027-07-06
Approved By: AIG Engineering

---

# Context

The AIG Platform requires a cloud infrastructure that provides predictable pricing, high performance, European data residency, and full operational control.

The infrastructure must support:

- Web applications
- Backend APIs
- AI services
- PostgreSQL databases
- Redis
- Object storage
- CI/CD
- Monitoring
- Future North Star services

---

# Decision

The primary cloud platform for Project Genesis will be Hetzner Cloud.

All production infrastructure will initially be deployed within European regions to simplify GDPR compliance and reduce latency for the initial target market.

---

# Reasons

Hetzner provides:

- Transparent pricing
- Excellent performance
- European data centers
- Strong Linux support
- Flexible networking
- High availability options
- Terraform compatibility
- Docker and Kubernetes compatibility

---

# Infrastructure Principles

Infrastructure shall be:

- Infrastructure as Code
- Reproducible
- Automated
- Version controlled
- Secure by default

Manual configuration should be minimized.

---

# Initial Platform

Production

- Reverse Proxy
- Application Servers
- PostgreSQL
- Redis
- Object Storage
- Monitoring
- Logging

Development

- Docker Compose
- Local PostgreSQL
- Local Redis

---

# Security

Infrastructure shall implement:

- Private networking
- Firewall rules
- SSH key authentication
- Secrets management
- Daily backups
- TLS encryption
- Audit logging

---

# Future Evolution

The architecture shall support migration toward Kubernetes if operational requirements justify the added complexity.

Infrastructure choices should avoid unnecessary vendor lock-in.

---

# Consequences

Positive

- Predictable costs
- Excellent performance
- Strong GDPR alignment
- Operational simplicity
- High flexibility

Trade-offs

- Smaller managed-service ecosystem than hyperscale providers
- More operational responsibility

---

# Review

Review annually or when infrastructure requirements change significantly.
