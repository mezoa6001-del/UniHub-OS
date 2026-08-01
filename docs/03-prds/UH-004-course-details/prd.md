# UH-004 — Course Details

**Document Type:** Product Requirements Document (PRD)

| Field | Value |
|-------|-------|
| Feature ID | UH-004 |
| Version | 1.0.0 |
| Status | Approved |
| Priority | P0 |
| Sprint | Sprint 02 |

---

# Executive Summary

The Course Details page provides complete information about a course before purchase and serves as the course homepage after enrollment.

Its purpose is to help students make informed enrollment decisions and quickly access course content.

---

# Business Goals

- Increase course conversion rate.
- Reduce purchase hesitation.
- Improve course completion.

---

# User Stories

As a visitor,

I want to see complete course information,

so that I can decide whether to enroll.

---

As an enrolled student,

I want to access course chapters,

so that I can continue studying.

---

# Functional Requirements

The page shall display:

- Course Title
- Course Description
- Instructor Information
- Course Thumbnail
- Number of Chapters
- Number of Lessons
- Estimated Duration
- Student Rating
- Student Reviews
- Enrollment Status

---

If the user is NOT enrolled:

Display

- Price
- Buy Button

---

If the user IS enrolled:

Display

- Continue Learning
- Course Content
- Progress

---

# Business Rules

Visitors cannot access lesson videos.

Only enrolled students can access lessons.

Hidden or unpublished courses cannot be accessed.

---

# Success Metrics

- Course Page Views
- Enrollment Conversion Rate
- Continue Learning Click Rate

---

# Acceptance Criteria

- Course data loads correctly.
- Enrollment status is accurate.
- Progress is displayed for enrolled users.
- Visitors cannot access locked lessons.

---

# Out of Scope

- Lesson Player
- Question Bank
- Certificates