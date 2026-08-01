# UH-006 — Question Bank API

Base URL

/api/v1/question-banks

---

GET /

Returns available question banks.

---

GET /{chapterId}

Returns chapter information.

---

POST /start-session

Creates a new question session.

---

Errors

401 Unauthorized

403 Enrollment Required

404 Chapter Not Found