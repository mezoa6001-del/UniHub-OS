# PROJECT_STRUCTURE.md

# UniHub Repository Structure

Version: 1.0

---

# Philosophy

The repository is organized around domains instead of technologies.

Every folder has one responsibility.

The structure should remain scalable for years.

---

# Root Structure

```
UniHub/

├── apps/
├── packages/
├── backend/
├── docs/
├── infrastructure/
├── scripts/
├── assets/
├── .github/
│
├── README.md
├── CLAUDE.md
├── AGENTS.md
├── CONTRIBUTING.md
├── LICENSE
├── CHANGELOG.md
└── PROJECT_STRUCTURE.md
```

---

# apps/

Contains all user-facing applications.

```
apps/

web/

student portal

admin/

platform administration

instructor/

instructor dashboard

mobile/

React Native application
```

Each application should be independently deployable.

---

# packages/

Shared code.

```
packages/

ui/

shared UI library

database/

Prisma schema

api/

shared API types

ai/

prompt library

shared/

utilities
```

---

# backend/

Contains backend services.

```
backend/

auth/

courses/

lessons/

questions/

analytics/

payments/

notifications/

community/

search/

knowledge/

ai/

media/

users/
```

Every service owns

Controllers

Services

Repositories

DTOs

Validation

Tests

---

# docs/

Official documentation.

```
docs/

00-manifesto/

01-business/

02-product/

03-prds/

04-architecture/

05-database/

06-api/

07-ai/

08-design-system/

09-roadmap/

10-meetings/

11-decisions/
```

---

# docs/03-prds/

Contains every Product Requirement Document.

```
PRD-001

Landing

PRD-002

Authentication

...

PRD-023

Database Architecture
```

Future PRDs continue sequentially.

---

# docs/04-architecture/

Contains

System Architecture

Backend

Frontend

Infrastructure

Deployment

Security

Event Bus

Microservices

Scalability

---

# docs/05-database/

Contains

ERD

Tables

Indexes

Relationships

Migration Strategy

Version History

Backup Strategy

---

# docs/06-api/

Contains

REST APIs

Authentication

Examples

Error Codes

Rate Limits

SDK

OpenAPI Specification

---

# docs/07-ai/

Contains

AI Architecture

Prompt Engineering

Agent System

Knowledge Graph

Medical Intelligence Engine

Adaptive Learning

Evaluation

Safety

---

# docs/08-design-system/

Contains

Colors

Typography

Spacing

Icons

Components

Buttons

Cards

Inputs

Tables

Accessibility

---

# docs/09-roadmap/

Contains

Vision

Quarterly Goals

Releases

Milestones

Future Features

---

# infrastructure/

Contains

Docker

Terraform

CI/CD

Monitoring

Logging

Cloud Configuration

---

# scripts/

Contains

Database Seeds

Migration Scripts

Maintenance Scripts

Automation Scripts

Development Helpers

---

# assets/

Contains

Brand Assets

Logos

Illustrations

Marketing

Icons

Social Media

PDFs

---

# .github/

Contains

GitHub Actions

Issue Templates

Pull Request Templates

CODEOWNERS

Security Policies

---

# Branch Strategy

```
main

Production

↓

develop

Main development

↓

feature/*

↓

bugfix/*

↓

hotfix/*
```

---

# Naming Convention

Folders

lowercase

Files

kebab-case

Components

PascalCase

Variables

camelCase

Constants

UPPER_CASE

Database

snake_case

---

# Documentation Rule

Every major feature must have

PRD

Architecture

Database

API

Acceptance Criteria

---

# Development Lifecycle

Idea

↓

PRD

↓

Architecture

↓

Database

↓

API

↓

Frontend

↓

Backend

↓

Testing

↓

Deployment

↓

Monitoring

---

# Definition of Done

A feature is only complete if

✓ PRD approved

✓ UI completed

✓ Backend completed

✓ Database migrated

✓ Tests written

✓ Documentation updated

✓ Performance verified

✓ Security reviewed

---

# Long-Term Goal

This repository should eventually contain everything required to operate UniHub.

A new engineer should be able to clone the repository and understand the entire platform from the documentation alone.