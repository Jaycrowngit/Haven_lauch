# Putting the SkyHaven coming-soon page live

This project builds to plain static files in `dist`. Any static host works. The three below have free plans and free HTTPS.

## Option 1: Netlify or Vercel, connected to GitHub (recommended)

1. Push this `site` folder to its own GitHub repository.
2. In Netlify or Vercel, choose **Add new site / project → Import from GitHub** and pick the repository.
3. Use these settings:

| Setting | Value |
|---|---|
| Base / root directory | leave empty |
| Build command | `npm run build` |
| Output / publish directory | `dist` |
| Node version | set the environment variable `NODE_VERSION` to `24` |

4. Optional environment variables: `PUBLIC_WAITLIST_ACTION` (turns on the "Notify me" form) and `PUBLIC_CONTACT_EMAIL`.
5. Every push to `main` redeploys the site.

## Option 2: Cloudflare Pages

Same settings: build command `npm run build`, output directory `dist`, environment variable `NODE_VERSION=24`.

## Option 3: Upload by hand (no GitHub)

In this folder, run:

```bash
npm run build
```

Then drag the `dist` folder onto Netlify Drop (app.netlify.com/drop), or upload its contents to any web host's public folder.

## Collecting "Notify me" emails

1. Create a free form at a form service such as Formspree.
2. Copy the form's endpoint URL, for example `https://formspree.io/f/abcdwxyz`.
3. Set it as `PUBLIC_WAITLIST_ACTION` in your host's environment variables, then redeploy.

## Connecting your domain

1. Buy the domain (for example `skyhavenhomes.com`, since `skyhaven.com` is taken).
2. In your host's dashboard, add the domain under **Domains**.
3. At your domain registrar, add the DNS records the host shows you. Usually that's an `A` record for the bare domain and a `CNAME` for `www`.
4. Wait for DNS to update (minutes to a few hours). HTTPS is issued automatically.
