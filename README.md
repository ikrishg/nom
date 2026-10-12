# Nom

How much do I love your name? Type a name and Nom gives it a score, then shows which letters and patterns added or took away points.

**Live:** [nom.krishg.com](https://nom.krishg.com)

## How the score works

The scoring lives in `app/lib/nom-lover.ts`. Each name is scored from:

- **Letters:** each vowel and consonant has its own score. For example, `a` and `e` add 10, `k` adds 25, `n` and `t` add 10, and `q` and `x` take away 2.
- **Adjacent vowels and adjacent consonants:** two vowels or two consonants side by side add the product of their scores. The `nn` in `Anna` adds 100.
- **Letter combinations:** clusters such as `bb`, `sch` or `rst` take away points.
- **Pairs of combinations:** two different combinations next to each other also count.
- **First letter:** some starting letters add or take away points.

The breakdown lists every rule with a nonzero score, with where it matched in the name. Rules that score zero, such as the letter `u`, are left out. It's a toy, so the numbers are opinion, not science.

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
