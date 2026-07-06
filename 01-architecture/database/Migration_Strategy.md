# Migration Strategy

Title: Migration Strategy
Version: 1.0.0
Status: Approved
Owner: AIG Engineering
Last Updated: 2026-07-06
Review Date: 2027-01-06
Approved By: AIG Engineering

## Purpose

This document defines how schema changes are introduced safely and consistently.

## Strategy

- Use versioned migrations
- Apply migrations through CI/CD
- Keep migrations reversible where possible
- Test migrations before production rollout
- Require review for schema changes affecting critical domains
