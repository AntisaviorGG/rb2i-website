# RB2I LLC — rb2i.com

Public website for **RB2I LLC** (Miramar, Florida), served by **GitHub Pages** at the custom domain **rb2i.com**.

## Contents

- `index.html` — the entire site: a single minimal page (inline CSS, no scripts, no external assets). Per Malachi's direction (Nov 24, 2026), the site stays as minimal as possible: RB2I LLC presented simply as **a developing software and engineering business** (Software Development · Engineering · Research & Development), Miramar, Florida. No product pages, no project details, no contact details.
- `CNAME` — GitHub Pages custom domain: `rb2i.com`
- `.nojekyll` — tells GitHub Pages to serve the files as-is (no Jekyll processing)

## Publishing

This folder is the repository root. To go live:

1. Create a **public** GitHub repository named `rb2i-website` and add it to the Muse GitHub App's repository access (GitHub Settings → Applications).
2. Push these files to the repository's default branch.
3. In the repo: **Settings → Pages** → deploy from the default branch (root). The `CNAME` file sets the custom domain to `rb2i.com` automatically.
4. At GoDaddy (registrar for rb2i.com), point DNS to GitHub Pages:
   - Apex `A` records: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - (Optional) `AAAA` records: `2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`, `2606:50c0:8003::153`
   - `www` as a `CNAME` to `<username>.github.io`
   - Remove any old hosting/parking records that conflict.
5. Back in **Settings → Pages**, tick **Enforce HTTPS** once the certificate provisions (can take up to ~24h after DNS propagates).

## Content rules

Minimal, public-knowledge only. The site presents RB2I LLC only as a developing software and engineering business. It must never include sensitive information: no patent or project details, no email addresses or other personal contact details, no addresses beyond city/state, no financial information, no other RB2I businesses, and no material from private plans.

## Contact form (added Nov 24, 2026; switched to FormSubmit Nov 27, 2026)
The home page has a "Send us a message" form. It posts via AJAX to
FormSubmit (https://formsubmit.co/ajax/<alias>), which delivers each
submission to soljjaboii1@gmail.com and CCs Malachi.Brown@yahoo.com — both
inboxes get every message (Malachi's direction, Nov 27, 2026). The form
carries only the public FormSubmit alias string
(e1e6aca9ecff8290f2eedc71011eab20); no destination email appears in the
form endpoint. The CC address sits in a `_cc` field in the submit script.

History: the form originally used Web3Forms with a placeholder key (never
activated). FormSubmit was chosen because Web3Forms charges for CC
delivery. Activation was anchored on the Gmail after FormSubmit's
activation emails to Yahoo were never delivered (two attempts, Nov 27).

## Legal page
`legal.html` — Terms of Use, message/submission terms (submissions are
non-confidential; no obligation to respond or use ideas), IP, disclaimers,
limitation of liability, indemnification, privacy policy, Florida governing
law. Linked from the footer and the contact section. It is a strong general
template, NOT attorney-reviewed; get a Florida business attorney to review
it before the ventures go public.
