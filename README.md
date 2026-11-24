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

## Contact form (added Nov 24, 2026)
The home page has a "Send us a message" form. It posts to Web3Forms
(https://api.web3forms.com/submit), which delivers submissions to the RB2I
team inbox (get.help.rb2i@gmail.com). The destination email appears NOWHERE
in the site files — the form carries only a public Web3Forms access key.

**Before go-live, one step:** get the access key from web3forms.com for the
RB2I inbox (they email it to that inbox), then replace
`WEB3FORMS_ACCESS_KEY_PENDING` in index.html with the key. Until then the
form will show a "could not be sent" message.

## Legal page
`legal.html` — Terms of Use, message/submission terms (submissions are
non-confidential; no obligation to respond or use ideas), IP, disclaimers,
limitation of liability, indemnification, privacy policy, Florida governing
law. Linked from the footer and the contact section. It is a strong general
template, NOT attorney-reviewed; get a Florida business attorney to review
it before the ventures go public.
