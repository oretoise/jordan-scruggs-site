Personal site for Jordan Scruggs — resume and project portfolio at [scruggs.dev](https://scruggs.dev).

Built with [Astro](https://astro.build) (based on the [Astro Nano](https://github.com/markhorn-dev/astro-nano) theme), Tailwind, and TypeScript.

## Content

- `src/consts.ts` — site name, email, social links
- `src/content/work/` — resume / work history entries
- `src/content/projects/` — project portfolio entries
- `src/content/blog/` — optional notes/articles (currently empty)
- `src/pages/index.astro` — homepage bio copy

## Local development

This project uses `pnpm`.

| Command             | Action                                      |
| :------------------- | :------------------------------------------ |
| `pnpm install`        | Install dependencies                        |
| `pnpm run dev`         | Start local dev server at `localhost:4321`  |
| `pnpm run build`       | Type-check and build to `./dist/`           |
| `pnpm run preview`     | Preview the production build locally        |
| `pnpm run lint`        | Run ESLint                                  |

## Deployment

Hosted on Cloudflare Pages.
