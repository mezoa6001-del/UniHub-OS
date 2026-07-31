# AGENTS.md

# UniHub AI Multi-Agent Architecture

Version: 1.0

---

# Philosophy

UniHub does not use a single AI assistant.

Instead, UniHub is powered by a team of specialized AI agents coordinated by one central orchestrator.

Each agent has one responsibility.

The Orchestrator decides which agents should collaborate to solve the user's request.

---

# AI Architecture

Student

↓

AI Gateway

↓

AI Orchestrator

↓

Specialized Agents

↓

Unified Response

---

# AI Gateway

Responsibilities

- Authentication
- Rate Limiting
- Conversation Management
- Context Loading
- Logging
- Cost Tracking

---

# AI Orchestrator

The Orchestrator is the brain of the AI system.

Responsibilities

- Intent Detection
- Agent Selection
- Context Collection
- Workflow Planning
- Response Merging
- Safety Validation

The Orchestrator never generates educational content directly.

---

# Tutor Agent

Purpose

Teach medicine.

Responsibilities

- Explain concepts
- Simplify difficult topics
- Clinical reasoning
- Drug mechanisms
- Pathophysiology
- Interactive teaching

Input

Lesson

Question

Student Profile

Knowledge Graph

Output

Educational explanation.

---

# Question Agent

Purpose

Assessment.

Responsibilities

- Generate MCQs
- Generate Clinical Cases
- Generate OSCE Stations
- Generate Flashcards
- Generate Rapid Review Questions

Difficulty Levels

Easy

Medium

Hard

USMLE

NBME

Clinical

---

# Flashcard Agent

Responsibilities

Generate

Basic Cards

Cloze Cards

Image Occlusion

Rapid Review Cards

Memory Hooks

Mnemonic Cards

---

# Planner Agent

Responsibilities

Generate

Daily Plan

Weekly Plan

Exam Plan

Revision Plan

Study Schedule

Recovery Plan

Uses

Exam Date

Weak Topics

Learning Speed

Available Time

---

# Mentor Agent

Purpose

Student motivation.

Responsibilities

- Build habits
- Reduce burnout
- Encourage consistency
- Celebrate achievements
- Adjust workload

Never

Provide fake motivation.

Always use real learning data.

---

# Analytics Agent

Responsibilities

Calculate

Mastery

Readiness

Weak Topics

Consistency

Predicted Performance

Learning Efficiency

---

# Knowledge Agent

Purpose

Structured medical knowledge.

Provides

Drug Information

Disease Information

Investigations

Guidelines

Learning Objectives

Relationships

Never invents medical facts.

---

# Research Agent

Responsibilities

Search

Medical References

Clinical Guidelines

Research Papers

Evidence

Provides

Citation-ready summaries.

---

# Search Agent

Responsibilities

Search

Courses

Lessons

Questions

Notes

Community

Flashcards

Knowledge Graph

Medical Entities

---

# Recommendation Agent

Purpose

Recommend

Lessons

Questions

Flashcards

Videos

Revision

Community Discussions

Recommendations are personalized.

---

# Community Agent

Responsibilities

Moderate

Detect spam

Detect misinformation

Suggest discussions

Generate summaries

---

# Instructor Agent

Supports instructors.

Generate

Slides

Questions

Objectives

Course outlines

Clinical cases

Analytics

---

# Admin Agent

Supports platform administrators.

Responsibilities

Reports

Monitoring

Alerts

Moderation

AI Usage

Content Quality

---

# Medical Validation Agent

One of the most important agents.

Responsibilities

Validate

Drug information

Guidelines

Clinical reasoning

References

Never allow hallucinated medical content.

Every educational response should pass through this agent whenever structured medical knowledge is available.

---

# Safety Agent

Responsibilities

- Policy checks
- Sensitive content detection
- Prompt injection protection
- Abuse prevention
- Output filtering

Runs before every response is delivered.

---

# Memory Agent

Stores

Short-Term Memory

Current Session

Recent Chats

Long-Term Memory

Learning Preferences

Study Goals

Weak Topics

Learning History

Student Progress

---

# Context Builder

Before every AI request

Collect

Current Course

Current Lesson

Current Question

Current Chapter

Knowledge Nodes

Student Profile

Recent Conversations

Weak Topics

Upcoming Exams

Then pass this context to the selected agents.

---

# Agent Communication Rules

Agents never communicate directly.

All communication must pass through the AI Orchestrator.

Benefits

- Easier debugging
- Better observability
- Lower coupling
- Higher scalability

---

# Failure Strategy

If one agent fails

↓

Retry

↓

Fallback Agent

↓

Cached Response

↓

Graceful Degradation

The platform should never completely fail because one agent becomes unavailable.

---

# Long-Term Vision

Future agents include

- Radiology Agent
- Pathology Agent
- Surgery Agent
- Anatomy Agent
- Pharmacology Agent
- Pediatrics Agent
- Cardiology Agent
- Hospital Protocol Agent
- Residency Advisor Agent
- Research Writing Agent
- Career Coach Agent

---

# Golden Rule

Every AI agent exists for one purpose only:

Help medical students learn better.

Not to impress them.

Not to replace their instructors.

Not to make medical decisions.

Only to improve learning.