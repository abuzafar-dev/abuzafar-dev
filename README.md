## Abuzafar Eshboboyev

**Python Backend Developer** · Django · Django REST Framework · PostgreSQL<br>
Tashkent, Uzbekistan · Software Engineering student at TUIT

[![Email](https://img.shields.io/badge/Email-abuzafareshboboyev1%40gmail.com-555?style=flat-square&logo=gmail&logoColor=white)](mailto:abuzafareshboboyev1@gmail.com)
[![Telegram](https://img.shields.io/badge/Telegram-%40Abuzafar__006-26A5E4?style=flat-square&logo=telegram&logoColor=white)](https://t.me/Abuzafar_006)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Abuzafar_Eshboboyev-0A66C2?style=flat-square)](https://www.linkedin.com/in/abuzafar-eshboboyev-abb5433b9/)

I build REST APIs and the business logic behind them: inventory, sales, payments
and reports for small shops. I care most about the parts that have to stay
correct when several people use the system at once. That means retried requests,
concurrent checkouts and per-tenant data isolation.

Looking for a **junior backend role** (Python / Django) or freelance backend work.

---

### Featured project

#### [Mening Bozorim](https://github.com/abuzafar-dev/my-market) — POS, inventory and credit ledger for small shops

A multi-tenant point-of-sale system that replaces the paper notebook in a small shop.

- **Stock from FIFO batches:** stock is calculated from purchase batches, sold oldest first, with expiry tracking
- **Idempotent checkout:** a retried sale returns the original receipt instead of charging twice
- **Credit ledger:** customer debts and payments, plus day/week/month reports with Excel and CSV export
- **JWT auth:** rotating refresh cookie, owner/seller roles, login lockout and rate limiting
- **Phone-first PWA:** barcode scanning with the phone camera, Uzbek and Russian UI

`Django 6` `DRF` `PostgreSQL` `JWT` `Vue 3` `Docker Compose` `GitHub Actions`
236 automated tests, including 34 security tests, run in CI on every push.

---

### Tech I use

| | |
|---|---|
| **Backend** | Python · Django · Django REST Framework · PostgreSQL · JWT · OpenAPI |
| **Tooling** | Docker · Docker Compose · GitHub Actions · Git · Linux · ruff |
| **Also used** | Vue 3 · Django Channels · FastAPI · aiogram |
| **Learning now** | Celery · Redis · production monitoring |

### Other repositories

Minimal starter templates I keep for new projects:
[DRF + OpenAPI](https://github.com/abuzafar-dev/APITemplate) ·
[Django Channels](https://github.com/abuzafar-dev/WebSocketTemplate) ·
[aiogram bot](https://github.com/abuzafar-dev/TelegramBotTemplate)

Problem solving: [LeetCode](https://leetcode.com/u/Abuzafar/)
