# 🟠 Reddit OS

**Score any Reddit post idea and rewrite weak titles with AI — before you launch into the algorithmic jungle.**

![License](https://img.shields.io/badge/license-MIT-blue) ![GitHub Pages](https://img.shields.io/badge/hosted-GitHub%20Pages-222?logo=github) ![No backend](https://img.shields.io/badge/backend-none-brightgreen) ![Built with Claude](https://img.shields.io/badge/AI-Claude%20Sonnet-blueviolet)

- 📊 **6-dimension engagement scoring** — weighted by post archetype, not a one-size-fits-all number

- ✦ **AI title rewriter** — 3 archetype-aware alternatives from Claude, click to apply and rescore instantly

- 🔍 **Anti-pattern detection** — flags weak openers, vague nouns, and title killers as you type

---

## Live demo

**[ohsusannamarie.github.io/reddit-os](https://ohsusannamarie.github.io/reddit-os)**

---
<!--
## Screenshots

| | |

|---|---|

| ![Scoring panel](screenshots/scoring.png) | ![AI rewriter](screenshots/ai-rewriter.png) |

| *6-dimension scoring with archetype-aware weights* | *AI title alternatives with one-click apply* |

| ![Anti-pattern detection](screenshots/antipatterns.png) | ![Preflight checklist](screenshots/preflight.png) |

| *Inline title analysis as you type* | *60-second preflight + clickable title templates* |

---
-->
## What it does

Reddit engagement isn't random. Posts succeed or fail based on a small set of structural signals — and most people only notice them in hindsight.

Reddit OS makes those signals visible before you post.

**Scoring engine**

- Scores your post across title strength, curiosity gap, credibility stack, conversation surface area, community fit, and readability

- Weight multipliers adjust per archetype — a Mystery post and an Analysis post earn engagement differently, so they're scored differently

- Fires suggestions only for dimensions that actually need work

**Title analysis**

- Live word counter with sweet-spot highlighting (8-14 words)

- Anti-pattern pills fire inline: weak openers, vague nouns, ends-with-?, starts-with-article

- 5 clickable title templates from the Reddit OS Field Manual — click to populate the title field

**AI title rewriter**

- Sends your title, archetype, subreddit, and body context to Claude Sonnet

- Returns 3 alternatives with named angles (constraint + tension, unexpected observation, earned authenticity, etc.)

- Click any result to apply it to the title field and auto-rescore

**Preflight checklist**

- 7-item checklist with strikethrough state

- Covers the full loop: title, evidence, conversation surface area, subreddit fit, mobile formatting, first-hour availability

---

## Tech stack

| Layer | Tech |

|---|---|

| Frontend | Vanilla HTML/CSS/JS — single file, zero build step |

| AI | Anthropic Claude Sonnet via `/v1/messages` |

| Storage | None — fully stateless |

| Fonts | Inter (system stack) |

| Hosting | GitHub Pages |

---

## Run it locally

```bash

git clone https://github.com/ohsusannamarie/reddit-os.git

cd reddit-os

# Option 1 — Python (built into Mac)

python3 -m http.server 8080

# then open http://localhost:8080

# Option 2 — just open the file (scoring works, AI rewriter requires a server or GitHub Pages)

open index.html

```

The AI title rewriter calls the Anthropic API from the browser. It works on GitHub Pages and localhost — not from a `file://` URL directly.

---

## Background

Built from the Reddit OS Field Manual — a framework covering post archetypes, the NEWS test (Novel, Evidence, Worth Discussing, Stake), credibility stacking, conversation surface area, and community matching. The scorer operationalizes those heuristics into a weighted, archetype-aware model.

This is a personal tool. It scratches a real itch. It's on GitHub Pages because things that work should be shareable.

---

## License

[MIT](LICENSE) — use freely, attribution appreciated.

---

*For everyone who has ever written a perfectly good post and watched it get 3 upvotes because the title asked "thoughts?" at the end.*
