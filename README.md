# Kasia i Michał — wedding invitation

A standalone, Polish- and English-language wedding invitation website for Kasia and Michał. It is a static site built with HTML, CSS, JavaScript, and locally stored artwork in `assets/`, maintained independently from the WeddingProject application.

## What the site includes

- Responsive invitation page, photo gallery, and Sicilian-inspired styling.
- Responsive envelope introduction and an interactive scratch-to-reveal card; the intro remains available with reduced motion enabled.
- Polish/English language switch in the header; the selected language is reflected in the page URL as `?lang=en`.
- Decorative Sicilian-inspired ticket frame surrounding the scratch-to-reveal card.
- Sicilian tile and olive artwork framing the wedding, gallery, and contact sections.
- Date, venue, address, map, calendar download, countdown, and schedule shown after the guest reveals the details.
- Travel guidance, accommodation recommendations, dress guidance, and gift information.
- WhatsApp RSVP links with pre-filled messages. Guests review and send the message themselves; the site does not send messages or collect RSVPs.
- Copy-to-clipboard support for the Revolut account number.
- A footer heart icon linking to the MedinaBytes GitHub profile.

The site has no database, authentication, server functions, analytics, or required API keys. No build step is required.

## Local preview

From the project directory, start Python's static file server:

```sh
python -m http.server 8765
```

Open [http://localhost:8765/](http://localhost:8765/) in a browser. Stop the server with `Ctrl+C`.

To preview the English version directly, open [http://localhost:8765/?lang=en](http://localhost:8765/?lang=en), or use the language switch in the header.

## Deploy to Vercel

### Using the Vercel CLI

1. Install the CLI and sign in:

   ```sh
   npm install --global vercel
   vercel login
   ```

2. From this directory, deploy a preview:

   ```sh
   vercel
   ```

3. Deploy to production when the preview is verified:

   ```sh
   vercel --prod
   ```

There is no build command or output-directory setting. Vercel serves `index.html`, `vercel.json`, and `assets/` directly.

### Using the GitHub repository

Import `rumbadelabuena/kasiawedding` as a new Vercel project. Keep the framework preset set to **Other** and leave the build command and output directory empty. Do not connect this project to the WeddingProject repository.

## Before publishing

Review the content in `index.html` and confirm all details are current:

- The event is listed for 5 June 2027 at 19:00 local Palermo time.
- Venue: Club Nautico Costa Ponente, Via Giuseppe Pavone, 91, 90151 Palermo PA, Italia.
- Confirm the Kasia and Michał WhatsApp phone numbers used by the RSVP links.
- Add the Polish- and English-language WhatsApp group links when available; the page currently has placeholder text for these.
- Confirm the Revolut account number and all travel, hotel, venue contact, and schedule information.
- Review the event date and location with the scratch card closed and after it is revealed, to ensure the intended details are shown correctly.

The HTML contains page metadata, Open Graph/Twitter URLs, and event structured data. If using a domain other than `kasiamichal.pl`, update the canonical URL, social preview URLs, and event URL in `index.html` to the actual public domain before publishing. Also verify the social preview image path and that the image is present in `assets/`.

## Files

- `index.html` — all page content, styles, structured event metadata, and client-side interactions.
- `assets/` — invitation artwork, photos, and decorative images.
- `vercel.json` — static hosting and response-header configuration.

## Browser checks

Before sharing a deployment, check both language versions at mobile and desktop widths. Verify the envelope intro and skip action, scratch interaction and reveal button, date/venue visibility, map and calendar links, localized WhatsApp RSVP messages, and account-number copy action. The scratch reveal and clipboard action require a browser with JavaScript enabled; clipboard access may require HTTPS or localhost.
