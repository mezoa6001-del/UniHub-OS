# UH-001 — Landing Page Database

Version: 1.0

Status: Draft

---

# Purpose

The Landing Page does not own any database tables.

It reads data from existing services.

---

# Tables Used

## courses

Used to display featured courses.

Fields

- id
- title
- slug
- thumbnail
- instructor_id
- price
- rating
- students_count
- is_featured

---

## instructors

Used to display instructor names.

Fields

- id
- full_name
- profile_image

---

## pricing_plans

Fields

- id
- name
- price
- duration
- description
- active

---

## testimonials

Fields

- id
- student_name
- university
- rating
- comment
- approved

---

## faqs

Fields

- id
- question
- answer
- display_order

---

# Relationships

courses
↓

instructors

Landing Page joins only the required fields.

---

# Database Rules

- Never query unpublished courses.
- Only approved testimonials are displayed.
- Only active pricing plans are returned.
- FAQs are ordered by display_order.

---

# Indexes

courses.is_featured

pricing_plans.active

testimonials.approved

faqs.display_order

---

# Future Improvements

- Hero content managed from CMS
- Landing banners
- Promotions
- Dynamic homepage sections