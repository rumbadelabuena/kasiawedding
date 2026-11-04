# Kasia i Michał — invitation website

A standalone, Polish-language wedding invitation built with static HTML, CSS, JavaScript, and local artwork in `assets/`.

## Deployment

This site is static and does not require a database, Supabase, server functions, or environment variables. The RSVP links open WhatsApp with a pre-filled message; guests send the message themselves.

### Deploy with Vercel

1. Install the Vercel CLI and sign in:

   ```sh
   npm install --global vercel
   vercel login
   ```

2. From this folder, create a preview deployment:

   ```sh
   vercel
   ```

3. Deploy to production:

   ```sh
   vercel --prod
   ```

There is no build command or output-directory setting: `index.html`, `vercel.json`, and `assets/` are served directly from this folder. Alternatively, put this folder in its own Git repository and import that repository into Vercel; do not use the WeddingProject repository.

Before sharing the site, confirm that `kasiamichal.pl` is the intended public domain. If the site will use a different domain, update the canonical URL, Open Graph/Twitter URLs, and event JSON-LD URL in `index.html` to match it.

## Local preview

From this folder, run:

```sh
python -m http.server 8765
```

Then open `http://localhost:8765/`.
