# Zumbrota Shoe & Leather Repair — Website

Website for Ansley Travo's cobbler shop in Zumbrota, MN.

Built with **Astro + Tailwind CSS**. Designed for static hosting on Netlify or Cloudflare Pages.

## Quick start

```sh
npm install
npm run dev
```

Open http://localhost:4321

## Project structure

```
src/
├── components/      Reusable bits (Nav, Footer)
├── layouts/         Page shell
├── pages/           One file per route (index, about, services, contact)
└── styles/          Global Tailwind + design tokens
public/
├── photos/          Site imagery — see public/photos/README.md
└── admin/           Decap CMS for content editing (Ansley)
```

## Adding photos

Drop image files into `public/photos/` using the exact filenames listed in
`public/photos/README.md`. The site references them directly.

## Deployment

### Recommended: Netlify

1. Push this repo to GitHub
2. In Netlify, "New site from Git" → select the repo
3. Build command: `npm run build`, publish directory: `dist`
4. Enable **Netlify Identity** + **Git Gateway** to give Ansley access to
   `/admin` for editing content.
5. Connect a custom domain (e.g. `zumbrotashoeandleather.com`)

### Alternative: Cloudflare Pages

Same build settings. Faster CDN, but Decap CMS auth needs GitHub OAuth setup.

## Contact form

The contact form posts to Formspree. Replace `REPLACE_WITH_FORMSPREE_ID` in
`src/pages/contact.astro` with a Formspree form ID after signing up at
formspree.io (free tier: 50 submissions/month).

## Design tokens

Colors defined in `src/styles/global.css`:
- `cream`, `paper` — backgrounds
- `ink`, `ink-soft` — text
- `oxblood` — primary accent (CTAs, links)
- `tan` — secondary accent (eyebrow text, dividers)
- `landis` — vintage green echoing the shop's Landis machines

Fonts: Cormorant Garamond (display), Inter (body).
