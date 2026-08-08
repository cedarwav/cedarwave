# Website Launch Plan — Consulting / AI Advisory Site

**Stack:** Astro (static site generator) → GitHub repo → GitHub Pages, auto-deployed via a GitHub Action. Edited locally in VS Code. Contact form via Web3Forms (emails submissions to you).

**How the work splits:** You handle accounts, installs, and content/assets. Claude generates the actual site code and gives you exact commands at each step.

---

## Phase 1 — Accounts & tools (one-time)

- [ ] Create a GitHub account and turn on 2FA.
- [ ] Install **Node.js** (LTS version) — this is what Astro runs on.
- [ ] Install **Git** — version control / how your site gets to GitHub.
- [ ] Install **VS Code** — your editor.
- [ ] (When you reach the contact page) create a free **Web3Forms** account and copy your access key.

_Once these are installed, come back to Claude to scaffold the project._

---

## Phase 2 — Content & assets (your real work)

Gather these before building — the tech is fast, good content is what takes time:

- [ ] Business name, tagline, and a 2–3 sentence "what we do."
- [ ] Canonical domain preference: `example.com` **or** `www.example.com` as primary (pick one).
- [ ] Copy for each page: **Home** (hero + value prop), **About** (bio / experience / credibility), **Services** (3–6 offerings, each with a short description), **Contact**.
- [ ] Visual assets: logo or wordmark, headshot (if personal-brand), 2–3 brand colors, font preference.
- [ ] 1–2 starter blog posts (even short) so the blog doesn't launch empty.
- [ ] The email address the contact form should deliver to.

---

## Phase 3 — Scaffold the project (Claude does this with you)

- [ ] Create a new GitHub repository.
- [ ] Claude generates the Astro project skeleton: layout, nav, and blog setup.
- [ ] Run it locally (one command) and confirm it previews in your browser.
- [ ] Commit and push the skeleton to GitHub.

---

## Phase 4 — Build pages, blog & contact

- [ ] Feed Claude your Phase 2 content; get the Home / About / Services / Contact pages back.
- [ ] Set up the blog: an index page + a template that turns each markdown file into a post.
- [ ] Wire the contact form to your Web3Forms access key (submissions email you — no server needed).
- [ ] Add a favicon and check the mobile layout.

---

## Phase 5 — Deploy to GitHub Pages

- [ ] In the repo's **Settings → Pages**, enable Pages.
- [ ] Add the GitHub Action file Claude gives you — it builds and publishes the site on every push (deployment becomes automatic from here on).
- [ ] Confirm the site works on the temporary `yourname.github.io/repo` URL **before** touching your domain.

---

## Phase 6 — Custom domain & HTTPS

- [ ] In **Settings → Pages**, enter your custom domain (GitHub adds a `CNAME` file for you).
- [ ] At your registrar's DNS panel, add:
  - Four `A` records (optionally `AAAA` for IPv6) pointing your apex domain at GitHub's Pages IPs.
  - A `CNAME` record for `www` → `yourname.github.io`.
  - _Get the exact current IP values from GitHub's "Managing a custom domain" docs at the time you do this — ask Claude to look them up so they're current._
- [ ] Wait for DNS to propagate (minutes to a few hours).
- [ ] Tick **Enforce HTTPS** once GitHub finishes issuing the certificate.
- [ ] Confirm the non-primary version (apex or www) redirects to your chosen canonical one.

---

## Phase 7 — Launch checklist

- [ ] Page titles + meta descriptions on every page.
- [ ] An Open Graph image (controls how your links look when shared).
- [ ] `sitemap.xml` and `robots.txt`.
- [ ] A custom 404 page.
- [ ] Privacy-friendly analytics (Plausible or Cloudflare Web Analytics — avoids cookie-banner hassle).
- [ ] Final pass: click every nav link, submit the contact form once (check the email lands), view on a phone.

---

## Phase 8 — Ongoing workflow (the "minimal updates" part)

- [ ] **New blog post** = add one markdown file, push. The Action rebuilds and redeploys in ~1–2 minutes.
- [ ] **Content edits** = edit the file, push. Same flow.
- [ ] Everything is in Git, so you get automatic version history and backups for free.

---

### Next action
Do Phase 1 (account + Node.js + Git + VS Code). Then come back and Claude will scaffold the project.
