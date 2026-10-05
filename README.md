<p align="center"><img src="assets/img/logo-wordmark.png" alt="Alex Gestalt Bots" width="160"></p>

# Alex Gestalt Bots: portfolio site

Portfolio site for **Alex Gestalt, chatbot & automation developer** (New York, USA). I build n8n workflows and chatbots, WhatsApp and Telegram bots, GoHighLevel bots, AI voice agents and lead-gen receptionist bots for small businesses.

- **Live demo:** `demo/`: *Ava*, an AI receptionist and lead-qualification chatbot for **Cedar & Pine Dental, a fictional business** made up for this demo
- **Contact:** gestaltworks@gmail.com · [fiverr.com/alex_gestalt](https://www.fiverr.com/alex_gestalt)
- **Fiverr gigs:**
  - [n8n AI chatbot](https://www.fiverr.com/alex_gestalt/build-an-n8n-ai-chatbot-that-qualifies-leads-and-books-appointments)
  - [WhatsApp AI bot](https://www.fiverr.com/alex_gestalt/build-a-whatsapp-ai-bot-that-answers-leads-and-books-appointments-24x7)
  - [GoHighLevel AI chatbot](https://www.fiverr.com/alex_gestalt/set-up-a-gohighlevel-ai-chatbot-that-qualifies-and-books-your-leads)

## Featured project: Ava, AI receptionist & lead-gen bot

> Portfolio demo for a fictional business. It is not a client project.

- Qualifies leads by name, service need, urgency and contact details
- Books appointment requests from available time slots
- The n8n workflow (`assets/files/ai-receptionist-n8n-workflow.json`) adds qualified leads to a Google Sheets spreadsheet and sends a lead summary by email/WhatsApp
- The browser demo is rule-based and runs entirely client-side, with no API keys. URL options: `?theme=whatsapp` (WhatsApp-style skin), `?autoplay=1` (scripted run), `&speed=0.3` (faster)

To import the workflow, go to n8n → *Workflows → Import from File*, connect your own credentials, and replace every `REPLACE_ME` / `REPLACE_WITH_*` placeholder. The file contains no API keys.

## Structure

```
index.html                 landing page
demo/index.html            Ava demo (single file, no dependencies)
assets/css/style.css       styles
assets/js/main.js          mobile menu + footer year
assets/img/                logo, favicons, Open Graph image, architecture diagram
assets/gigs/               service overview graphics (WebP)
assets/video/              47 s demo video (MP4, H.264) + poster
assets/files/              n8n workflow JSON
assets/favicon.ico
.nojekyll                  tells GitHub Pages to serve files as-is
```

Plain HTML, CSS and JS with no build step. Every path is relative, so the site works at `https://<user>.github.io/<repo>/` and on a custom root domain. The font is Plus Jakarta Sans from Google Fonts, with a system-font fallback.

## Run locally

```bash
python3 -m http.server 8000
# open http://localhost:8000/
```

## Deploy to GitHub Pages

1. Push this folder to a GitHub repository (the files must be at the repo root).
2. Go to **Settings → Pages → Build and deployment**, choose *Deploy from a branch*, then pick `main` and `/ (root)`.
3. Optional: once you know the final URL, change `og:image` / `twitter:image` in `index.html` to an absolute URL (e.g. `https://<user>.github.io/<repo>/assets/img/og-image.jpg`). Some social networks ignore relative image URLs in link previews.

## License / credits

© Alex Gestalt. Cedar & Pine Dental, Ava and the sample people in the demo are fictional.
