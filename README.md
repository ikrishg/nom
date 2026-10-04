# Nom

Toy web app: type a name and get a playful “how much I love this name” score, with a breakdown of which letters and patterns contributed (`app/lib/nom-lover.ts`).

**Live:** [nom.krishg.com](https://nom.krishg.com)

## Run locally

Requires [Bun](https://bun.sh/).

```bash
bun install
bun run dev
```

Dev server: `http://localhost:5173`. Production build: `bun run build` (static client output in `build/client`, used by the GitHub Pages workflow).
