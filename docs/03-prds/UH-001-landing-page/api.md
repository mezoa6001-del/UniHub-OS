# UH-001 — Landing Page API

Version: 1.0

Status: Draft

---

# Purpose

These endpoints provide all data required to render the Landing Page.

The Landing Page should never contain hardcoded content except static UI text.

---

# Base URL

/api/v1

---

# API Overview

| Endpoint | Method | Authentication |
|----------|--------|----------------|
| /landing | GET | No |
| /courses/featured | GET | No |
| /pricing | GET | No |
| /testimonials | GET | No |
| /faq | GET | No |

---

# GET /landing

## Purpose

Returns general landing page content.

### Response

```json
{
  "hero": {
    "title": "Learn Medicine Smarter",
    "subtitle": "Courses, Question Bank and AI in one platform",
    "primaryCTA": "Start Learning",
    "secondaryCTA": "Explore Courses",
    "image": "/hero.png"
  }
}
```

---

# GET /courses/featured

## Purpose

Returns featured courses.

### Response

```json
[
  {
    "id": "course_001",
    "title": "General Pharmacology",
    "instructor": "Dr. Ahmed",
    "price": 499,
    "rating": 4.9,
    "students": 1245,
    "thumbnail": "/courses/pharma.png"
  }
]
```

---

# GET /pricing

## Purpose

Returns active subscription plans.

### Response

```json
[
  {
    "id": "basic",
    "name": "Basic",
    "price": 199,
    "features": [
      "Access to selected courses"
    ]
  }
]
```

---

# GET /testimonials

## Purpose

Returns student testimonials.

### Response

```json
[
  {
    "name": "Ahmed",
    "university": "Menoufia University",
    "rating": 5,
    "comment": "Excellent explanation."
  }
]
```

---

# GET /faq

## Purpose

Returns FAQ list.

### Response

```json
[
  {
    "question": "Can I watch on mobile?",
    "answer": "Yes."
  }
]
```

---

# Error Response

```json
{
  "success": false,
  "message": "Internal Server Error"
}
```

---

# Performance Requirements

- Average response < 300ms
- Cached where possible
- CDN for images
- GZIP enabled

---

# Security

- HTTPS only
- Rate limiting
- Input validation
- No sensitive data exposed

---

# Future Endpoints

- GET /landing/personalized
- GET /landing/recommendations
- GET /landing/promotions