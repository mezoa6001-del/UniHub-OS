# UH-009 — Payment API

POST /payments

Create payment.

---

GET /payments/{paymentId}

Returns payment status.

---

POST /payments/{paymentId}/verify

Verify completed payment.

---

Errors

401 Unauthorized

402 Payment Required

404 Payment Not Found