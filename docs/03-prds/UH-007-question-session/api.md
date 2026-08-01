# UH-007 — Question Session API

Base URL

/api/v1/question-sessions

---

POST /

Create Session

---

GET /{sessionId}

Load Session

---

PATCH /{sessionId}/answer

Save Answer

---

POST /{sessionId}/submit

Submit Session

---

GET /{sessionId}/result

Load Results

---

Errors

401 Unauthorized

404 Session Not Found

409 Session Already Submitted