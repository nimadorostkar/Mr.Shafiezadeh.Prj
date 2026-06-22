# Personal Knowledge · Digital Garden · Personal Archive

> One connected mind with three editorial policies — not a three-section website.

A personal, content-first platform that unifies **Knowledge** (working memory, editable forever), **Garden** (thinking in public, maturity-staged), and **Archive** (the immutable record) into a single content graph you fully own.

## Core idea

These aren't three apps — they're **one content graph with three editorial policies** (mutability, visibility, truth conditions). Content migrates between them. The body lives as **Markdown-in-Git**, so it outlives every tech choice and walks out the door as `.md` anytime.

| Pillar | Lifecycle | Default |
|---|---|---|
| 🧠 Knowledge | Editable forever, author-first | Private |
| 🌱 Garden | Maturity-staged (🌱→🌿→🌳), public dialogue | Opt-in public |
| 🗄️ Archive | Append-only, provenance-preserving | Immutable |

## Stack

`Django + DRF` · `PostgreSQL (+ pgvector)` · `React` · `Celery + Redis` · `Markdown + Git` (canonical content) · `Docker Compose` · `nginx`

## Roadmap

`P0` Foundation → `P1` Knowledge (private-first) → `P2` Garden → `P3` Archive → `P4` Graph + Discovery → `P5` SEO + Polish

> **Rule:** earn the next pillar by proving the last one gets used daily. Content systems die from disuse, not bad code.

## AI (future, removable)

A lens over the graph you own — `pgvector` embeddings, ask-my-notes RAG with citations, link suggestion, maturity nudges. **Privacy boundary = routing boundary**: private content never leaves your box. Turn it off and nothing breaks.

## Deploy

Runs on an Iranian VPS (low local latency, ریال billing). Build images in **CI**, push to a registry, **pull** on the VPS to dodge flaky upstream egress (Docker Hub / PyPI / npm). Keep Markdown backed up off-box in Git.

```bash
docker compose up   # web · db · redis · celery · nginx
```

## Principles

- **Content outlives code** — Markdown-in-Git is the source of truth; the DB is a rebuildable index.
- **Capture friction is the enemy** — optimized for adding the 500th note at 11pm.
- **Longevity is a feature** — clean export path is a first-class requirement.

## License

TBD
