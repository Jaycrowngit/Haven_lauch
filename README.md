# SkyHaven site

The coming-soon page for the SkyHaven domain, built with Astro. It becomes the marketing site later.

## Run it

```bash
npm install
```

```bash
npm run dev
```

Open http://localhost:4321.

## Change the page

The whole page is `src/pages/index.astro`. Brand colours are in `src/styles/tokens.css`. The logo and icons are in `public/`.

## Settings (optional)

Copy `.env.example` to `.env`:

- `PUBLIC_WAITLIST_ACTION`: a form address from a form service such as Formspree. Turns on the "Notify me" email form.
- `PUBLIC_CONTACT_EMAIL`: shows a contact email in the footer.

## Put it live

See [DEPLOY.md](DEPLOY.md).
