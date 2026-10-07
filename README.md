## Abuzafar Eshboboyev

**Junior Python / Django backend developer.** I build JSON APIs with Django REST
Framework on PostgreSQL, and I care most about the parts that are easy to get
wrong: transactions, concurrency, and whether the thing actually holds up under
two requests arriving at once.

```
Python · Django · Django REST Framework · PostgreSQL · Docker · GitHub Actions
```

---

### Mening Bozorim — [`my-market`](https://github.com/abuzafar-dev/my-market)

A POS, inventory and debt-ledger system for small shops. Django 6 + DRF
JSON-only API, a separate Vue 3 PWA frontend, PostgreSQL, Docker Compose, CI.

**8,400 lines of Python · 236 tests · 33 commits**

What is worth looking at in it:

- **Stock is never a stored column.** It is summed live from FIFO batches, so
  there is exactly one source of truth, with database-level `CheckConstraint`s
  keeping it non-negative rather than trusting application code.
- **Checkout is idempotent** on a client-generated id. The read that looks it up
  is only a fast path — the real guard is a unique constraint plus a savepoint,
  so the request that loses the race unwinds its own stock consumption instead
  of double-selling.
- **Concurrent tills cannot deadlock each other.** Cart lines are merged and
  locked in a fixed order, so two checkouts touching the same two products
  always take their row locks in the same sequence.
- **Cancelling a receipt re-reads it under a row lock**, so two cancel requests
  credit the stock back once, not twice.
- **Auth and abuse handling:** JWT with rotating, blacklisted refresh tokens in
  an httpOnly cookie, a login-lockout authentication backend, per-scope
  throttling, and owner/seller role permissions.
- **Reports** for any day, week or month, with Excel and CSV export.
- **Operations:** split settings per environment, nothing secret in source,
  security headers and HSTS in production, a `/healthz/` check, and CI that runs
  ruff lint, format checking, a missing-migrations check and the suite.

Written in Uzbek for the shopkeeper, in English for whoever reads the code.

---

### Django starter templates

Small, deliberately minimal starting points — each one wires up a single thing
properly and nothing more.

| Repo | What it sets up |
|---|---|
| [`APITemplate`](https://github.com/abuzafar-dev/APITemplate) | DRF + OpenAPI docs (drf-spectacular), health check, tests |
| [`DockerAPITemplate`](https://github.com/abuzafar-dev/DockerAPITemplate) | The same, Dockerized with PostgreSQL, gunicorn, WhiteNoise |
| [`django-graphql-template`](https://github.com/abuzafar-dev/django-graphql-template) | Graphene GraphQL CRUD with the GraphiQL explorer |
| [`WebSocketTemplate`](https://github.com/abuzafar-dev/WebSocketTemplate) | Django Channels: ASGI consumer, routing, Redis channel layer |
| [`docker-django-jinja-template`](https://github.com/abuzafar-dev/docker-django-jinja-template) | Django rendering through Jinja2 instead of DTL |
| [`TelegramBotTemplate`](https://github.com/abuzafar-dev/TelegramBotTemplate) | aiogram 3 long polling, config from `.env` |

### Also here

[`Janona-Market`](https://github.com/abuzafar-dev/Janona-Market) — a
server-rendered Django e-commerce and affiliate platform: customer storefront,
seller cabinet with referral funnels and commissions, and an operator panel for
processing orders. Broader in features than `my-market`, simpler in engineering.

---

### What I am working on next

- Moving `my-market`'s report exports onto **Celery + Redis**, so a large Excel
  file stops holding a request open
- A **Telegram companion bot** for `my-market` — daily takings, low stock and
  outstanding credit over the existing API

### Contact

**Email** — abuzafareshboboyev1@gmail.com
