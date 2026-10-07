## Abuzafar Eshboboyev

Junior Python / Django backend developer.

**Stack:** Python · Django · Django REST Framework · PostgreSQL · Docker · GitHub Actions

---

### Mening Bozorim — [`my-market`](https://github.com/abuzafar-dev/my-market)

A POS, inventory and debt-ledger system for small shops: a JSON-only Django 6 +
DRF API with a separate Vue 3 PWA frontend, on PostgreSQL.

Stock is never stored as a column — it is summed live from FIFO batches, so there
is one source of truth, with `CheckConstraint`s enforcing it at the database
level. Checkout is idempotent on a client-generated id (`unique_together` plus a
savepoint that unwinds the stock consumption when a retry loses the race), and
cart lines are locked in a fixed order so two tills cannot deadlock each other.

JWT auth with rotating, blacklisted refresh tokens in an httpOnly cookie; a
login-lockout authentication backend; per-scope throttling; role-based
permissions (owner / seller); Excel and CSV report exports.

**236 tests** (`manage.py test`), and CI that runs ruff lint, ruff format
checking, a missing-migrations check, the test suite, and the frontend lint and
build.

---

### Templates

Small, deliberately minimal starters I keep for new projects:

| Repo | What it is |
|---|---|
| [`APITemplate`](https://github.com/abuzafar-dev/APITemplate) | Django REST Framework + OpenAPI docs |
| [`DockerAPITemplate`](https://github.com/abuzafar-dev/DockerAPITemplate) | The same, Dockerized with PostgreSQL and gunicorn |
| [`django-graphql-template`](https://github.com/abuzafar-dev/django-graphql-template) | Django + Graphene GraphQL CRUD |
| [`WebSocketTemplate`](https://github.com/abuzafar-dev/WebSocketTemplate) | Django Channels, ASGI consumer, Redis channel layer |
| [`docker-django-jinja-template`](https://github.com/abuzafar-dev/docker-django-jinja-template) | Django rendering with Jinja2 |
| [`TelegramBotTemplate`](https://github.com/abuzafar-dev/TelegramBotTemplate) | aiogram 3 long-polling skeleton |

---

### Contact

- **Email** — abuzafareshboboyev1@gmail.com
