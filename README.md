# Hodge Insurance · Performance Reports

Static site for the Hodge Insurance GOAL campaign reports. No build step.

```
index.html            Landing page with a card for each report
reports/marketplace.html    Home marketplace, last 3 months
reports/deep-dive.html      Property type, property age, county, source
reports/inbound-calls.html  Inbound calls, last 180 days, with 75% / 90% answer rate scenarios
reports/quote-bind.html     Home marketplace quote and bind analysis, Sep 4 to Oct 31, 2026
reports/action-plan.html    Action plan for contact, quote, and bind rate, Sep 4 to Oct 31, 2026
assets/               GOAL logos used by the landing page
vercel.json           Clean URLs (/reports/auto) and noindex headers
```

## Deploy on Vercel

Import the repo in Vercel with Framework Preset **Other**, leave Build Command and Output Directory empty, and deploy. Or from the CLI: `vercel --prod`.

Search engines are blocked (`robots.txt` + `X-Robots-Tag`), but the URL is public to anyone who has it. Turn on Vercel Deployment Protection if the reports need a login.

## Adding a report

Drop the HTML file into `reports/` with a lowercase, hyphenated name, then add a card for it in `index.html`.

Source exports live in `marketplace-exports/`. They are git-ignored and excluded from deploys (`.vercelignore`) because they include bid data that must never be public.
