# UniHub AI Rules

Version: 1.0

Status: Active

Applies To

- Claude
- ChatGPT
- Codex
- Cursor
- GitHub Copilot
- Any AI used within UniHub

---

# Purpose

This document defines how AI assistants must behave while working on UniHub.

AI is part of the engineering team.

It must follow the same standards as human developers.

---

# Primary Objective

Help build the best medical education platform.

Not the fastest.

Not the cheapest.

The best.

---

# Core Rule

Never optimize for speed at the expense of quality.

---

# Source of Truth

When information conflicts, follow this order:

1. UNIHUB_OS.md
2. PRDs
3. Architecture Documents
4. API Specifications
5. Database Schema
6. Existing Code

Never ignore a higher-priority document.

---

# Before Writing Code

Always:

- Read the relevant PRD.
- Understand the feature.
- Check dependencies.
- Follow the existing architecture.

Never start coding immediately.

---

# Architecture Rules

Never change architecture without explaining why.

Never introduce unnecessary complexity.

Prefer modular design.

Prefer reusable components.

Keep features independent.

---

# Coding Standards

Write production-ready code.

Use TypeScript.

Use strict typing.

Avoid duplicated logic.

Prefer composition over duplication.

Write readable code.

Follow project naming conventions.

---

# Frontend Rules

Use reusable UI components.

Follow the design system.

Keep pages responsive.

Optimize performance.

Avoid unnecessary re-renders.

Never hardcode business logic inside UI components.

---

# Backend Rules

Business logic belongs in Services.

Controllers should remain thin.

Validate all inputs.

Return consistent API responses.

Handle errors gracefully.

---

# Database Rules

Never expose sensitive data.

Use migrations.

Prefer indexes for frequent queries.

Never delete production data without approval.

---

# Security Rules

Validate every input.

Authenticate every protected endpoint.

Authorize every sensitive action.

Never expose secrets.

Never commit API keys.

---

# Testing Rules

Every feature should include:

- Unit Tests
- Integration Tests (where appropriate)

Do not consider a feature complete until it has been tested.

---

# Documentation Rules

Keep documentation updated when implementation changes.

If documentation and code conflict, report it.

Do not silently ignore inconsistencies.

---

# Medical Content Rules

Medical accuracy is mandatory.

Never invent medical facts.

When uncertain, state uncertainty clearly.

Never present guesses as facts.

---

# Marketing Rules

Follow MARKETING.md.

Follow BRAND_GUIDELINES.md.

Never produce misleading content.

Never use fake urgency.

Never exaggerate outcomes.

---

# AI Behavior

If requirements are unclear:

Ask questions.

Do not guess.

If multiple solutions exist:

Explain trade-offs.

Recommend the best option.

---

# Code Review Checklist

Before considering work complete:

- Clean Architecture
- Readable Code
- No Duplication
- Error Handling
- Security
- Performance
- Responsive Design
- Accessibility (Frontend)
- Tests
- Documentation Updated

---

# Git Rules

Small commits.

Meaningful commit messages.

Never modify unrelated files.

Respect branch strategy.

---

# Definition of Done

A task is complete only if:

- Requirements satisfied
- Code reviewed
- Tests passed
- Documentation updated
- No critical issues remain

---

# Final Rule

Always optimize for long-term maintainability.

Build software that the team will be proud to maintain five years from now.