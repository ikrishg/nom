# Nom

How much do I love your name? Type a name and Nom gives it a score, then shows which letters and patterns added or took away points.

**Live:** [nom.krishg.com](https://nom.krishg.com)

## How the score works

The scoring lives in `app/lib/nom-lover.ts`. Each name is scored from:

- **Vowels:** for example, `a` and `e` add 10, `u` adds nothing.
- **Consonants:** for example, `k` adds 25, `n` and `t` add 10, `q` and `x` take away 2.
- **Letter combinations:** clusters such as `bb`, `sch` or `rst` take away points.
- **Repeated combinations** and **the first letter** also count.

The breakdown lists every rule that fired, with its score and position in the name. It's a toy, so the numbers are opinion, not science.

## Stack

- React Router 7 (framework mode) with React 19
- Bun for installs and scripts
- Static build deployed to GitHub Pages by `.github/workflows/deploy.yaml` on every push to `main`

## Run locally

Requires [Bun](https://bun.sh/).

```bash
bun install
bun run dev        # http://localhost:5173
bun run typecheck  # React Router typegen, then tsc
bun run build      # static client output in build/client
```
