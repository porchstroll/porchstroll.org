# porchstroll.org

This is the source for [porchstroll.org](https://porchstroll.org) — the governance and transparency site for [porchstroll](https://porchstroll.com), a privacy-first social network.

## why this is public

porchstroll's whole pitch is "we don't use you." Anyone can say that. This repo is one small way to back it up: the site that makes our transparency claims is itself something you can read, verify, and hold us to.

This is a static site on purpose. No JavaScript, no external requests, no analytics, no font or CDN calls, no access logging on the server. What you see in this repo is what gets served — there's no build step hiding anything from you.

## what's here

- `index.html` — landing page
- `governance.html` — how porchstroll is structured and governed
- `transparency.html` — open questions, decisions made, and decisions still pending (see status-tag system below)
- `faq.html`
- founder's letter

## status tags

Pages on this site — especially the transparency page — use a simple tag system to be honest about where things stand:

- **Decided** — settled, in effect
- **Committed** — the direction is set, details are still being worked out
- **Still deciding** — genuinely open, no answer yet

We'd rather show you an honest "still deciding" than a confident answer we made up to look finished.

## running it locally

No build tools, no dependencies. Clone it and open `index.html` in a browser, or serve the directory with anything that speaks static HTML (we use [Caddy](https://caddyserver.com/) in production, with no access-log directive — we don't collect visitor IPs even for our own site).

```bash
git clone https://github.com/porchstroll/porchstroll.org.git
cd porchstroll.org
python3 -m http.server 8000
```

## license

MIT — see [LICENSE](./LICENSE).

## questions or found something off?

If you spot a claim on this site that doesn't hold up, or copy that's inconsistent with how porchstroll actually operates, we want to know. Open an issue.
