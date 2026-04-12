<p align="center">
  <h1 align="center">VERSO</h1>
  <p align="center">
    <strong>Track what you watch, play, and read AND then actually remember it.</strong>
  </p>
  <p align="center">
    <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/license-MIT-blue?style=flat-square" alt="License"></a>
    <img src="https://img.shields.io/badge/TypeScript-strict-blue?style=flat-square" alt="TypeScript">
    <img src="https://img.shields.io/badge/stage-alpha-orange?style=flat-square" alt="Stage: Alpha">
  </p>
  <p align="center">
    <a href="https://twitter.com/LeDevNovice">Follow the build</a>
  </p>
</p>

> **Verso is in active development. This project is being built in public by a solo developer. Not ready for external use yet.**

## The problem

You finished a 40-hour game three months ago. Who directed it ? What inspired it ? Why did it matter ?

You can't remember... and that's normal. We lose **most parts of what we consume within a week** without active reinforcement. Every existing tracker : Letterboxd, Goodreads, Backloggd, counts what you consumed and assigns it a number. None of them helps you **understand or retain** any of it.

The gap between _"I watched 200 films this year"_ and _"I deeply understand cinema"_ is not addressed by any platform.

## What Verso does

Verso combines three layers that no existing product brings together :

### Layer 1 : Track

Cross-media logging with dated sessions, progress tracking, and import from Letterboxd, Goodreads, MAL, Trakt, and Backloggd. A tier-based ranking system (S/A/B/C/D/F) replaces arbitrary numerical scores because ranking produces more reliable data than rating.

### Layer 2 : Deepen

When you finish a work, Verso reveals its other side : who made it and why, where it sits in its medium's history, what influenced it and what it influenced, the craft behind it, and even one killer anecdote you can retell at dinner if you want.

### Layer 3 : Retain

Auto-generated flashcards using the **testing effect** scheduled via **spaced repetition**. A daily 2-minute quiz keeps your cultural knowledge alive without feeling like homework.

## Getting started

```bash
git clone https://github.com/LeDevNovice/verso.git
cd verso
pnpm install
pnpm dev
```

Prerequisites: Node.js 22+, pnpm 9+, Docker (for PostgreSQL + Redis)

## Contributing

Verso is a solo project in its early stages, but feedback is welcome :

- **Ideas and suggestions** → [Discussions](https://github.com/LeDevNovice/verso/discussions)
- **Bug reports** → [Issues](https://github.com/LeDevNovice/verso/issues)
- **Follow the build** → [@LeDevNovice](https://twitter.com/LeDevNovice)

## License

[MIT](./LICENSE)

<p align="center">
  <em>Culture deserves to be retained, not just consumed.</em>
</p>
