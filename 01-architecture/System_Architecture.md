# System Architecture

Version: 1.0.0
Status: Approved
Owner: AIG Engineering
Last Updated: 2026-07-06
Review Date: 2027-01-06
Approved By: AIG Engineering

---

# Purpose

This document defines the high-level architecture of the AIG Platform and the North Star ecosystem.

It serves as the primary architectural reference for all engineering teams.

---

# Architectural Principles

The platform is designed according to the following principles:

- Security by Design
- Privacy by Design
- API First
- Domain Driven Design
- Cloud Native
- Modular Services
- Infrastructure as Code
- Documentation as Code
- Continuous Delivery
- Zero Trust Security

---

# High-Level Architecture

North Star Devices

¦

¦

Ask Diana Platform

¦

+--------------------------------------------+
¦              ¦              ¦              ¦
¦ Marketplace  ¦ Academy      ¦ Memberships  ¦
¦              ¦              ¦              ¦
+--------------------------------------------+

¦

Identity Platform

¦

PostgreSQL • Redis • Object Storage

¦

Hetzner Cloud Infrastructure

---

# Core Components

## Identity

Responsible for:

- Authentication
- Authorization
- Roles
- Organizations
- Sessions
- Devices
- Audit Logs

Identity is the foundation of every other service.

---

## Marketplace

Responsible for:

- Products
- Categories
- Vendors
- Orders
- Reviews

---

## Academy

Responsible for:

- Courses
- Videos
- Certifications
- Learning Progress

---

## Ask Diana

Responsible for:

- AI conversations
- Knowledge retrieval
- Prompt orchestration
- Conversation history
- User preferences

---

## North Star

Responsible for:

- Companion experience
- Device synchronization
- Voice interface
- Personal memory
- Secure cloud synchronization

---

# Infrastructure

Cloud Provider

- Hetzner Cloud

Container Platform

- Docker

Future Option

- Kubernetes

Database

- PostgreSQL

Cache

- Redis

Storage

- S3-compatible Object Storage

Monitoring

- Prometheus
- Grafana

Logging

- Centralized structured logging

---

# Security

Every request passes through Identity.

All communication uses TLS.

Secrets are never stored in source code.

Every significant action is audit logged.

Least privilege is the default permission model.

---

# Deployment Strategy

Development

?

Testing

?

Staging

?

Production

Deployment shall be fully automated through CI/CD.

---

# Scalability

Every service should be independently scalable.

Stateless services are preferred.

Persistent state belongs in dedicated storage systems.

---

# Future Expansion

The architecture is designed to support:

- Mobile applications
- Desktop applications
- North Star devices
- AI model abstraction
- Multiple languages
- International deployments

---

# Success Criteria

A successful implementation provides:

- High availability
- Strong security
- Modular development
- Operational simplicity
- Long-term maintainability

---

# Related Documents

- ADR-0001 Project Genesis
- ADR-0002 Domain Driven Repository Strategy
- ADR-0003 Hetzner Cloud Infrastructure
- ADR-0004 Identity First Architecture
