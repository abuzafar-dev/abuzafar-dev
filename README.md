## Abuzafar Eshboboyev

Backend developer — Python and Django. Based in Tashkent, Uzbekistan.

I am a Software Engineering student at TUIT, and I have been learning backend
development at PDP Academy alongside it. Most of what I actually know, though,
came from building two systems end to end and running into the problems you
only meet once something has real data in it.

What I keep coming back to is the part of a system that has to stay correct
when more than one person uses it at the same moment: a sale rung up twice
because a request was retried, a receipt cancelled from two tills at once, a
stock count that drifts because two requests read it before either one wrote.
Getting those right taught me more than any feature did.

I build for shops and small businesses here, which sets the constraints: it has
to work on an inexpensive phone, over unreliable Wi-Fi, for someone who has
never used a POS before.

I am looking for a junior backend position where I can work on real systems and
learn from people who have run them in production.

### What I work with

| | |
|---|---|
| **Daily** | Python · Django · Django REST Framework · PostgreSQL |
| **Comfortable** | Docker · Git · GitHub Actions · Linux · JWT auth · REST API design |
| **Enough to be useful** | Vue 3 · Jinja2 · GraphQL · Django Channels · aiogram |
| **Learning now** | Celery · Redis · deployment and monitoring in production |

I write tests for the parts that matter and I leave the reasoning in comments,
because I have already been the one working out why past-me did something.

### Things I have built

**[Mening Bozorim](https://github.com/abuzafar-dev/my-market)** · Sept 2026 — present
A POS, inventory and credit-ledger system for small shops — it replaces the
paper notebook. FIFO batch stock with expiry tracking, idempotent checkout that
holds under concurrent tills, a customer credit ledger, and sales reports
exported to Excel or CSV. Products are scanned with the phone camera, so the
shop needs no extra hardware. Django, DRF, PostgreSQL, JWT, Vue 3, PWA, Docker,
GitHub Actions CI. 236 tests, 34 of them covering per-shop data isolation,
login lockout and rate limiting.

**[Janona Market](https://github.com/abuzafar-dev/Janona-Market)** · Aug 2026
A multi-role e-commerce and dropshipping platform: sellers publish referral
landing pages, operators claim and fulfil orders from a shared queue, and a
ledger settles seller payouts. Full-stack Django.

**Starter templates** — small, deliberately minimal starting points I keep for
new projects: [DRF + OpenAPI](https://github.com/abuzafar-dev/APITemplate),
[the same Dockerized](https://github.com/abuzafar-dev/DockerAPITemplate),
[GraphQL](https://github.com/abuzafar-dev/django-graphql-template),
[Channels](https://github.com/abuzafar-dev/WebSocketTemplate),
[Jinja2](https://github.com/abuzafar-dev/docker-django-jinja-template),
[aiogram](https://github.com/abuzafar-dev/TelegramBotTemplate).

Each repository's README explains what it does and shows it running.

### Contact

Tashkent, Uzbekistan

- **Email** — abuzafareshboboyev1@gmail.com
- **Telegram** — [@Abuzafar_006](https://t.me/Abuzafar_006)
- **LinkedIn** — [abuzafar-eshboboyev](https://www.linkedin.com/in/abuzafar-eshboboyev-abb5433b9/)
- **LeetCode** — [Abuzafar](https://leetcode.com/u/Abuzafar/)
