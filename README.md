## Abuzafar Eshboboyev

**Python Backend Developer** · Django · Django REST Framework · PostgreSQL<br>
Tashkent, Uzbekistan · Software Engineering student at TUIT

[![Email](https://img.shields.io/badge/Email-abuzafareshboboyev1%40gmail.com-555?style=flat-square&logo=gmail&logoColor=white)](mailto:abuzafareshboboyev1@gmail.com)
[![Telegram](https://img.shields.io/badge/Telegram-%40Abuzafar__006-26A5E4?style=flat-square&logo=telegram&logoColor=white)](https://t.me/Abuzafar_006)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Abuzafar_Eshboboyev-0A66C2?style=flat-square)](https://www.linkedin.com/in/abuzafar-eshboboyev/)

I build REST APIs and the business logic behind them: inventory, sales, payments
and reports. I care most about the parts that have to stay correct when several
people use the system at once. That means retried requests, concurrent checkouts
and per-tenant data isolation.

Looking for a **junior backend role** (Python / Django) or an internship in Tashkent.

### Now

- Building **ZUNO**, an affiliate cash-on-delivery storefront
- Testing **Bog'la** on real phones before a public release
- Co-building a real-estate platform with a small team (early stage)
- Studying backend development at PDP Academy alongside university

---

### Featured projects

#### [Mening Bozorim](https://github.com/abuzafar-dev/my-market) — POS, inventory and credit ledger for small shops · `Completed · v1.0.0`

A multi-tenant point-of-sale system that replaces the paper notebook in a small shop.

- **Stock from FIFO batches:** stock is calculated from purchase batches, sold oldest first, with expiry tracking
- **Idempotent checkout:** a retried sale returns the original receipt instead of charging twice
- **Credit ledger:** customer debts and payments, plus day/week/month reports with Excel and CSV export
- **Background work:** Excel reports are built by a Celery worker; optional WhatsApp debt reminders; daily database backups
- **JWT auth:** rotating refresh cookie, owner/seller roles, login lockout and rate limiting
- **Phone-first PWA:** barcode scanning with the phone camera, Uzbek and Russian UI

`Django 6` `DRF` `PostgreSQL` `Celery` `Redis` `JWT` `Vue 3` `Docker Compose` `GitHub Actions`
429 automated tests run in CI on every push.

---

#### [ZUNO](https://github.com/abuzafar-dev/zuno) — Affiliate cash-on-delivery storefront · [project page](https://abuzafar-dev.github.io/zuno/) · `In progress`

An online store where partners sell through personal links and earn commission on every delivered order.

- **Money ledger:** every balance change is journaled, and a database constraint blocks double commission
- **Stock under concurrency:** row locks reserve items, so the last unit sells once (covered by parallel tests)
- **Order state machine:** stock returns and commission reversals are tied to status transitions
- **Three interfaces:** customer storefront with no-account checkout, partner cabinet, call-centre panel

`Django 6` `PostgreSQL 18` `Redis` `Docker` `GitHub Actions`
59 automated tests run against PostgreSQL in CI on every push.

---

#### Bog'la — Android phone and Linux PC, no cloud · [presentation](https://github.com/abuzafar-dev/bogla-taqdimot) · `Side project · v1`

Notifications, calls, SMS, file transfer and a shared clipboard between an Android phone
and a Linux computer over the local network, encrypted with TLS. No cloud and no account.

`Python asyncio` `Kotlin` `Material 3` `TLS` `mypy --strict`
The code is private for now; the presentation describes how it works.

---

### Tech I use

| | |
|---|---|
| **Backend** | Python · Django · Django REST Framework · PostgreSQL · Celery · Redis · JWT · OpenAPI |
| **Tooling** | Docker · Docker Compose · GitHub Actions · Git · Linux · pytest · ruff |
| **Also used** | Vue 3 · Django Channels · FastAPI · GraphQL · aiogram |
| **Learning now** | Production deployment · monitoring |

### Other repositories

Minimal starter templates I keep for new projects:
[DRF + OpenAPI](https://github.com/abuzafar-dev/APITemplate) ·
[Docker + DRF](https://github.com/abuzafar-dev/DockerAPITemplate) ·
[Django + Jinja2](https://github.com/abuzafar-dev/DockerDjangoJinjaTemplate) ·
[Django Channels](https://github.com/abuzafar-dev/WebSocketTemplate) ·
[GraphQL](https://github.com/abuzafar-dev/GraphqlTemplate) ·
[FastAPI](https://github.com/abuzafar-dev/FastAPITemplate) ·
[aiogram bot](https://github.com/abuzafar-dev/TelegramBotTemplate)

Problem solving: [LeetCode](https://leetcode.com/u/Abuzafar/)
