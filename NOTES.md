# Executive Car World — site notes

Static site, no build step. Open `index.html` directly, or serve the folder:

```bash
python3 -m http.server 8080
```

Pages: `index.html`, `services.html`, `parts.html`, `about.html`, `contact.html`, `credits.html`.
Assets: `assets/css/styles.css`, `assets/js/main.js`, `assets/img/*`, `favicon.svg`.

Deployment: `vercel.json` adds security headers and a one-hour cache on `/assets`.
`.vercelignore` keeps `screenshots/`, this file and `.freebuff/` off the public URL.

---

## Confirmed facts used on the site

Each item below is taken from a first-party Executive Car World page or post.

| Fact | Source |
|---|---|
| Location: Ridgeways, Kiambu Road, opposite Total Ridgeways, Nairobi | https://www.facebook.com/ExecutiveCarWorld/videos/welcome-to-executive-car-world-ltd-at-ridgeways-kiambu-road-opposite-total-petro/1892421790810953/ |
| Telephone 0790 007 007 and 0117 007 007 | https://www.instagram.com/executivecarworld/ |
| Email executivecarworldltd@gmail.com | https://www.instagram.com/executivecarworld/ |
| Tyre sales, fitting, puncture repair, wheel alignment and balancing | https://www.instagram.com/p/CYv1OULo6ZG/ |
| Repair and maintenance, oil changes | https://www.facebook.com/ExecutiveCarWorld/posts/1829074110588746/ |
| Minor and major car repair | https://www.facebook.com/ExecutiveCarWorld/posts/1753674418128716/ |
| Car wash | https://www.facebook.com/ExecutiveCarWorld/posts/1829074110588746/ |
| Body repair, accident repair, respray | https://www.facebook.com/ExecutiveCarWorld/posts/1721995834629908/ |
| Car lights sold and repaired | https://www.facebook.com/ExecutiveCarWorld/videos/842262839922512/ |
| Dedicated gearbox repair facility | https://www.instagram.com/reel/DZ95wNwswbv/ |
| Facelift kits and accessories | https://www.facebook.com/ExecutiveCarWorld/posts/1829074110588746/ |
| Products: spare parts, accessories, lighting, rims and tyres, cars | https://www.instagram.com/p/DcTon70MoQV/ |
| Batteries, suspensions, 4x4 accessories | https://www.facebook.com/ExecutiveCarWorld/posts/2196003587229128/ |
| Quad bikes, TGT products, breakdown services (own service list) | https://www.facebook.com/ExecutiveCarWorld/videos/executive-car-world-ltd/991020298409312/ |
| "50+ countries" (used on the About page) | https://www.instagram.com/executivecarworld/reels/ |
| Facebook, Instagram, TikTok, YouTube accounts | as linked in the site footer |

---

## Claims that did **not** verify — deliberately kept off the site

These came from an AI-generated Google Business summary, not from the business.
A second research pass found no first-party support for any of them, so they are
not published. If the owner confirms them in writing, they can go on the About
page as plain sentences (no code changes needed):

1. Founded in 2015 — **no source found.**
2. "84,000+ happy customers" — **no source found.**
3. "21,000+ vehicles worked on" — **no source found.**
4. "Family-owned business" — **no source found.**
5. "50+ countries" — **supported** by their own Instagram copy, and used.
6. Hours 9:00–18:00 six days a week — supported by their own 2023 post for the
   **Ngong Road showroom**, and kept on this site with soft wording. Confirm the
   Kiambu Road garage keeps the same hours (a third-party listing shows Saturday
   closing at 17:00).
7. Facebook 13,059 likes / 158 check-ins — page now reports 12,872 followers and
   177 visits. Social counts drift; none are published.

### Other open items

- **WhatsApp.** Not shown anywhere — no WhatsApp-enabled number was confirmed.
  Kenyan customers will look for one; add it to the contact page when known.
- **Second branch (Ngong Road, next to Shell Junction Mall).** Announced publicly
  and still promoted in 2024. Deliberately not listed, because it is unclear
  whether it is still trading.
- **Online store.** `executivecarworld.store` exists but returned a payment error
  when checked; `executivecarworld.co.ke` did not resolve. No store link is used.
- **M-Pesa, delivery, warranty, returns, wholesale/export terms.** None verified,
  so none are mentioned — these are the questions visitors will still have.

---

## Photography

Ten freely licensed photographs from Wikimedia Commons, stored in `assets/img/`,
with author and licence in `assets/img/credits.json` and on `credits.html`.

Images are shown high-contrast black and white (`.photo`) so mixed sources read
as one voice. To show them in colour, delete `class="photo"` from the `<img>`.

They are **stand-ins** — none shows the actual shop. Replace them with the
business's own photographs of the building, the bays, the counter and completed
work, keeping the same filenames and no code changes. The businesses' own
Facebook and Instagram feeds are the best source for those.

Photographs appear on every page: a full-bleed strip under the home hero, the
two doors on the home page, and a three-up `.band` gallery on each interior page.
Altitude labels are descriptive only — no photo is captioned as this workshop.

## Design system

- **Palette:** bitumen `#15171a`, concrete `#d7d8d4`, paper `#f4f3ee`,
  safety amber `#efa100`, steel `#6b7076`.
- **Type:** Archivo (variable width axis, expanded for display) + Newsreader
  (body serif). Loaded from Google Fonts; system fallbacks declared.
- **Signature elements:** hazard-stripe rules between sections, the data plate
  (equipment-plate treatment for address/hours/contact), the rotating technical
  wheel drawing in the home hero, asymmetric dark/amber "doors", and the
  full-bleed amber-hairline photo bands.
- **Motion:** one element only — the hero wheel's slow rotation. Everything is
  disabled under `prefers-reduced-motion`.
