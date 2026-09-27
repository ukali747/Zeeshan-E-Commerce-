# Zeeshan E-commerce — website

A TanStack Start (React) site: LTD formation, identity verification, TikTok
Agency accounts, Shopify dropshipping, digital marketing, Payoneer, and
YouTube automation service pages.

## Important — this is not a static site

This app has a server (TanStack Start + Nitro) and a database layer. **GitHub
Pages cannot host it** — GitHub Pages only serves plain HTML/CSS/JS files.
Use GitHub only to store the code, and deploy it on a host that runs Node
(Vercel is already configured below).

## Run it locally

```bash
npm install
npm run dev
```

Open http://localhost:8080

## Deploy (Vercel — free)

1. Push this repo to GitHub (see below).
2. Go to https://vercel.com → sign in with GitHub.
3. **Add New → Project** → import this repo.
4. Click **Deploy** — the build command and output are already configured
   via `vercel.json` and the Nitro `vercel` preset in `vite.config.ts`.
5. You'll get a free live URL like `your-project.vercel.app`.

No environment variables are required for the default setup (no sign-in,
no external database — it falls back to an embedded PGLite database). Only
add `DATABASE_URL` if you connect a real Postgres database later.

## Push this project to GitHub

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

## Project structure

- `src/routes/` — pages (file-based routing)
- `src/lib/site.ts` — all site content: services, fees, packages, FAQs, etc.
- `src/components/` — UI components
- `migrations/` — database migrations (only used if `DATABASE_URL` is set)
