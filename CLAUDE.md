# CLAUDE.md

# UniHub Engineering Context

This document provides the complete project context for AI coding assistants
(Claude, Codex, Cursor, GitHub Copilot, ChatGPT).

Always follow these instructions before generating code.

---

# Project Name

UniHub

---

# Vision

UniHub is not an online course website.

UniHub is building the Operating System for Medical Education.

The current product starts as a medical learning platform.

The long-term vision is an AI-powered ecosystem connecting students,
instructors, universities, hospitals, and medical knowledge.

---

# Current Product Scope (MVP)

The MVP includes

- Authentication
- Student Dashboard
- Course Platform
- Lesson Player
- Question Bank
- Question Session
- Instructor Dashboard
- Admin Dashboard
- Subscription System
- Notification System

Everything else should be designed to support future expansion.

---

# Product Philosophy

Always prioritize

1. Learning Experience

2. Simplicity

3. Performance

4. Scalability

5. Medical Accuracy

Never sacrifice learning quality for unnecessary features.

---

# Architecture

The project follows a modular architecture.

Every module owns its own domain.

No module should directly manipulate another module's internal data.

Modules communicate through APIs and events.

---

# Technology Stack

Frontend

- Next.js
- React
- TypeScript
- Tailwind CSS

Backend

- NestJS
- PostgreSQL
- Prisma
- Redis

Storage

- Firebase Storage

Authentication

- Firebase Auth

Payments

- Stripe
- Fawry
- Instapay
- Vodafone Cash

Deployment

- Docker
- Vercel
- Railway

---

# Coding Principles

Always

- Write clean code
- Prefer readability
- Keep functions small
- Avoid duplication
- Strong typing
- Reusable components
- Consistent naming

Never

- Hardcode secrets
- Use any type unless unavoidable
- Ignore error handling
- Ignore validation
- Mix business logic with UI

---

# Folder Structure

apps/

packages/

backend/

docs/

assets/

scripts/

---

# UI Principles

Mobile First

Responsive

Accessible

Minimal

Medical-focused

Professional

---

# Component Rules

Components must

- be reusable

- be isolated

- have typed props

- avoid unnecessary state

---

# Backend Rules

Use

Controllers

↓

Services

↓

Repositories

↓

Database

Business logic belongs inside services.

---

# Database Rules

Every table

- UUID primary key

- createdAt

- updatedAt

Soft delete whenever possible.

Never expose internal IDs to clients unnecessarily.

---

# API Standards

REST

Versioned

/api/v1/

Every response

{
  success,
  data,
  error
}

---

# AI Principles

AI assists learning.

AI never replaces medical references.

Whenever possible

AI responses should reference

- Knowledge Graph
- Medical Intelligence Engine
- Course Context
- Student Progress

---

# Question Bank Rules

Every question must contain

- Difficulty
- Learning Objective
- Knowledge Node
- Explanation
- Incorrect Explanation
- References

---

# Course Rules

Every lesson should contain

- Learning Objectives
- Video
- Transcript
- Resources
- AI Context

---

# Performance Targets

Initial page

<2 seconds

Question load

<500 ms

API

<300 ms

Search

<250 ms

---

# Security

Validate every input.

Never trust client data.

Use RBAC.

Use JWT.

Audit important actions.

Encrypt sensitive data.

---

# Documentation

Every major feature must include

- PRD

- Database changes

- API endpoints

- Acceptance criteria

---

# Git Workflow

main

production

develop

active development

feature/*

new features

bugfix/*

bug fixes

---

# Commit Style

feat:

fix:

refactor:

docs:

test:

style:

perf:

---

# Long-Term Goal

Every engineering decision should move UniHub closer to becoming

"The Operating System for Medical Education."