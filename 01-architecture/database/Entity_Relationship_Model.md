# Entity Relationship Model (ERM)

Version: 1.0.0
Status: Draft
Owner: AIG Engineering
Last Updated: 2026-07-06
Review Date: 2027-01-06
Approved By: Pending

---

# Purpose

This document defines the core business entities of the AIG Platform.

These entities represent business concepts rather than database tables. They form the foundation for the database schema, APIs, services, and user experience.

---

# Design Principles

The model follows these principles:

- Business-driven design
- Single source of truth
- Identity-first architecture
- Minimal duplication
- Auditability
- Extensibility

---

# Core Entity Overview

Person
¦
+-- Identity
+-- Organization
+-- Membership
+-- Role
+-- Permission
+-- Device
+-- AI Companion
+-- Conversation
+-- Consent
+-- Subscription
+-- Wallet
+-- Notification
+-- Audit Log

---

# Person

Represents a real human being.

A person may have:

- Multiple identities
- Multiple organizations
- Multiple memberships
- Multiple devices
- Multiple subscriptions

Primary Key:

PersonId (UUID)

---

# Identity

Represents authentication and login.

Contains:

- Email
- Password Hash
- MFA Configuration
- Login History
- Recovery Methods

Relationship:

One Person ? Many Identities

---

# Organization

Represents companies, associations, teams, or communities.

Relationships:

Many Persons ? Many Organizations

---

# Membership

Represents participation within AIG.

Examples:

- Free
- Premium
- Business
- Partner
- Founder

Membership is independent of Identity.

---

# Role

Defines responsibilities.

Examples:

- Member
- Administrator
- Moderator
- Vendor
- Instructor
- Support

---

# Permission

Defines capabilities.

Examples:

- Create Product
- Publish Course
- Manage Users
- Approve Vendors

Roles consist of collections of permissions.

---

# Device

Represents any connected client.

Examples:

- Browser
- Android
- iPhone
- Desktop
- North Star

Each device belongs to a Person.

---

# AI Companion

Represents the user's personal assistant.

Stores:

- Personality configuration
- Preferences
- Voice settings
- Language
- Memory references
- Safety settings

An AI Companion belongs to one Person but may synchronize across multiple devices.

---

# Conversation

Stores interactions between a Person and the AI Companion.

Contains:

- Messages
- Attachments
- Actions
- Citations
- Conversation metadata

---

# Consent

Stores legal consent records.

Contains:

- Consent Type
- Timestamp
- Version
- Jurisdiction
- Source
- Status

Required for GDPR compliance.

---

# Subscription

Represents recurring commercial services.

Contains:

- Plan
- Status
- Renewal Date
- Billing Provider

---

# Wallet

Represents balances, credits, and future digital assets.

Designed for future expansion.

---

# Notification

Represents platform communications.

Examples:

- Email
- Push Notification
- SMS
- In-App Notification

---

# Audit Log

Stores immutable security events.

Every significant action should generate an audit entry.

Examples:

- Login
- Password Change
- Consent Update
- Role Assignment
- Payment
- AI Configuration Change

---

# Entity Relationships

One Person

?

Many Devices

?

Many Conversations

?

Many Messages

One Person

?

Many Organizations

?

Many Roles

?

Many Permissions

One Person

?

One AI Companion

?

Many Memories

?

Many Conversations

---

# Future Entities

Reserved for future development:

- Marketplace Product
- Vendor
- Course
- Certificate
- Event
- Support Ticket
- AI Skill
- AI Plugin
- Workflow
- Knowledge Base

---

# Next Steps

The logical data model described here will be transformed into:

- PostgreSQL schema
- Entity definitions
- API contracts
- Service boundaries
- Migration scripts
