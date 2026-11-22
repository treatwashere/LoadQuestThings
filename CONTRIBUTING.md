# Contributing

## Local development

The web installer is built with **Vite + React**, using Bun, TanStack Query, and TanStack Store. To run it locally:

```bash
git clone https://github.com/treatwashere/LoadQuestThings.git
cd LoadQuestThings
bun install
bun run dev
bun run build
bun run preview
```

`bun run dev:brand` serves the design system preview (`apps/brand`). The shared tokens and components live in `packages/ui`.

## Cloudflare Workers deployment

Pushes to `main` deploy `apps/web` as Cloudflare Worker static assets at
[questload.nerdcoder.dev](https://questload.nerdcoder.dev), through `.github/workflows/deploy.yml`.
The `nerdcoder.dev` zone must be on the same Cloudflare account as the Worker; Cloudflare creates
the DNS record and certificate on the first deploy.

The workflow needs two GitHub Actions secrets, `CLOUDFLARE_ACCOUNT_ID` and `CLOUDFLARE_API_TOKEN`.
Set them with:

```bash
bun run credentials
```

It reads your `gh` and `wrangler` logins, explains what the token must be allowed to do, links to a
pre-filled token form, checks the token against Cloudflare, and stores both secrets on this repository.


The web installer is built with **Vite + React**, using Bun, TanStack Query, and TanStack Store. To run it locally:

```bash
git clone https://github.com/treatwashere/LoadQuestThings.git
cd LoadQuestThings
bun install
bun run dev
bun run build
bun run preview
```

`bun run dev:brand` serves the design system preview (`apps/brand`). The shared tokens and components live in `packages/ui`.

