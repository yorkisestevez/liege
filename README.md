# Liege

**The marketing team your business can't afford yet.**

Liege is a local-first AI marketing operations toolkit — 13+ specialized agents (copywriter, social manager, review responder, invoice collector, ads manager, and more) that run on your own computer and publish through your existing stack (WordPress, Webflow, Meta, Mailchimp, Google Business Profile).

Built for contractors, clinics, and solo operators who know they need consistent marketing but don't have time to post, respond, and follow up.

![Landing page](https://openclaw.yorkisestevez.com/og.png)

---

## Quick Links

| | |
|---|---|
| **Website** | https://openclaw.yorkisestevez.com |
| **Docs** | https://openclaw.yorkisestevez.com/docs |
| **Waitlist** | https://openclaw.yorkisestevez.com/#waitlist |
| **Pricing** | Starter $197/mo · Pro $497/mo · Agency $1,497/mo · Self-host FREE |

---

## What's in this repo

This repo is the **landing page + marketing site** for Liege. The core product (80+ agent skills, Command Deck UI, orchestration layer) lives separately and is published to GitHub closer to public beta.

```
landing/
├── index.html          Main landing page
├── pricing.html        (placeholder — detailed tier comparison)
├── docs/               (placeholder — install + troubleshooting)
├── netlify.toml        Deploy + forms config
├── LICENSE             MIT
└── README.md
```

---

## Local dev

Plain static HTML — no build step.

```bash
# From the landing/ directory:
npx http-server . -p 5056 -c-1

# Or just open index.html in your browser.
```

Tailwind is loaded via CDN for now. Will be pre-built when docs site lands.

---

## Deploy

Two paths:

### Option A — GitHub + Netlify (recommended, auto-deploys on push)
```bash
# 1. Create a public GitHub repo called `openclaw`
gh repo create yorkisestevez/openclaw --public --source=. --remote=origin --push

# 2. Connect in Netlify
#    - app.netlify.com → Add new site → Import from Git
#    - Choose this repo
#    - Build command: (leave blank)
#    - Publish directory: .
#    - Deploy

# 3. Point your domain
#    - Netlify → Domain settings → Add custom domain
#    - Enter: openclaw.yorkisestevez.com
#    - Add CNAME at your DNS provider:
#        openclaw   CNAME   <your-site>.netlify.app
#    - SSL provisions automatically
```

### Option B — Netlify drop (fastest, zero config)
```bash
# Drag-drop the landing/ folder at https://app.netlify.com/drop
# Add custom domain openclaw.yorkisestevez.com in the site settings.
```

---

## Waitlist form

Netlify Forms handles submissions automatically — no backend needed. Submissions appear in your Netlify dashboard under **Forms → waitlist**.

Set an email notification so new signups ping you:
- Netlify → Forms → Notifications → Email notification → your address.

---

## Positioning

**Pitch:** The marketing team your business can't afford yet.

**Buyer:** Ontario home-service contractors (landscaping, HVAC, roofing) first. Expansion to clinics, agencies, and regulated SMBs once the vertical hits $5K MRR.

**Differentiator:**
1. Runs locally on your hardware (client data never leaves)
2. Bills flat monthly (no per-token bills)
3. Publishes through your existing stack (never hosts your site)
4. Offers one-time $3,500 site rebuild for customers with unsalvageable sites

**Not:**
- Not a Wix/Webflow competitor
- Not Lindy or Relevance (horizontal, cloud-first)
- Not an AI writer (Jasper/Copy.ai)
- Not an agency at agency prices ($3-15K/mo)

---

## Roadmap (public)

- [x] Command Deck dashboard (13 wired agents, 80-skill library)
- [x] FB/IG OAuth + live publishing
- [x] Gmail + Calendar OAuth + 4 Gmail agents
- [x] Landing page + positioning
- [ ] Deploy to openclaw.yorkisestevez.com (this week)
- [ ] Install docs + AI chatbot + phone line (week 2)
- [ ] Migration agents: site-crawl, SEO audit, WP/Webflow publishers, GBP (week 3)
- [ ] First paid pilot at $497/mo (week 4)
- [ ] Public OSS release of core (after first 5 paid pilots)

---

## License

MIT. See [LICENSE](./LICENSE).

---

## Built by

[Yorkis Estevez](https://yorkisestevez.com) — solo builder in Barrie, ON.
Originally built to run marketing for [Golden Maple Landscaping](https://goldenmaplelandscaping.ca). Now opening to other local businesses that want their own private AI marketing team.
