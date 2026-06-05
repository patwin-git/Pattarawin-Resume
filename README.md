# Pattarawin Teerachai — Executive Portfolio

A polished, single-page personal portfolio website for **Pattarawin Teerachai**, Senior Manager — New Service & Content Business at LINE Company (Thailand). Built as a lightweight static site (HTML, CSS, vanilla JS) with no build step and no frameworks, so it deploys instantly on GitHub Pages.

## Features

- **Sticky navigation** with smooth scrolling, active-section highlighting, and a mobile menu.
- **Premium executive hero** with large serif typography, soft abstract background shapes, and a framed profile area.
- **About / professional summary** presented as a confident executive overview.
- **Career snapshot** — verified, metrics-style stat cards (no invented figures).
- **Experience timeline** — a vertical timeline with a green accent line; LINE and Starcom show multiple roles under one company.
- **Areas of expertise** — interactive skill chips with hover states.
- **Education** card with degree, year, GPA, and activities.
- **Contact section** with location, LinkedIn, and an editable email placeholder.
- Subtle scroll-reveal animations, hover effects, a back-to-top button, and full **reduced-motion** support.
- Fully **responsive** (polished two-column desktop hero → single-column mobile) and built with **semantic, accessible** HTML.

## File structure

```
.
├── index.html        # Page markup and content
├── styles.css        # All styling and design tokens
├── script.js         # Nav state, mobile menu, scroll reveal, back-to-top
├── assets/
│   ├── profile.jpg   # (add your photo here — see below)
│   └── README.md     # Photo instructions
└── README.md
```

## Run locally

No build tools required. Either:

- **Open directly:** double-click `index.html`, or
- **Serve locally** (recommended, so smooth scrolling and fonts behave like production):

  ```bash
  # Python 3
  python3 -m http.server 8000
  # then visit http://localhost:8000
  ```

## Deploy on GitHub Pages

1. Push these files to the **root** of the `main` branch of your repository.
2. On GitHub, go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Set the branch to **`main`** and the folder to **`/ (root)`**, then **Save**.
5. After a minute, your site is live at:
   `https://patwin-git.github.io/Pattarawin-Resume/`

## Update resume content

All content lives in plain text inside **`index.html`** — there is no CMS or data file to learn. Find the relevant `<section>` (each is clearly commented, e.g. `<!-- ===== Experience ===== -->`) and edit the text directly. To add an experience entry, copy an existing `<li class="t-item">…</li>` block in the timeline and update its company, role, dates, and location.

## Add or replace the profile photo

1. Save your portrait as **`assets/profile.jpg`** (about 800 × 1000 px, 4:5 ratio works best).
2. In `index.html`, inside the `.photo-frame` block, uncomment:

   ```html
   <img src="assets/profile.jpg" alt="Portrait of Pattarawin Teerachai" />
   ```

3. The image fills the framed card automatically. If you leave it out, a clean `PT` placeholder is shown instead.

## Update the contact email

Open `index.html` and find the **Contact** section (`<!-- ===== Contact ===== -->`). In the email card, update **both** the link target and the visible text:

```html
<!-- Update the email below: replace the href and the visible text with a real address -->
<a class="contact__card" href="mailto:add-email-here@example.com">
  <span class="contact__label">Email</span>
  <span class="contact__value">Add email address here</span>
</a>
```

Replace `add-email-here@example.com` in the `href` with the real address, and replace `Add email address here` with the address (or a label like “Email me”).

---

© Pattarawin Teerachai · Bangkok, Thailand
