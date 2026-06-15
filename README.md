# Shreyas Raorane Portfolio

Personal portfolio site for Shreyas Raorane, robotics software engineer (M.S.E. Robotics, UPenn GRASP Lab). Focus areas: multi-agent coordination, motion planning, and ROS2 autonomy.

## Stack

A single static file, `index.html`, with all CSS and JavaScript inline. No build step, no dependencies, no framework. Fonts load from Fontshare (Cabinet Grotesk, Satoshi) and Google Fonts (IBM Plex Mono); everything else is self-contained.

## Structure

The page is one `index.html` containing:

- **Hero**: intro, links, and a decorative terminal card (hidden below 1024px)
- **About**: research direction and focus, with a publications list
- **Experience**: industry roles (OPEX, Brillio)
- **Research & Teaching**: GRASP Lab thesis, F1/10 RoboRacer RA, teaching
- **Projects**: six selected technical projects
- **Skills**: languages, planning/control, multi-agent, tools, systems
- **Contact**: email (copy-to-clipboard), GitHub, LinkedIn

Inline scripts handle: runtime email assembly (basic bot-scraping mitigation), copy-email, the mobile nav menu, the scroll progress bar, and nav scrollspy.

## Files

- `index.html`: the entire site
- `favicon.svg`: favicon
- `Resume_Raorane.pdf`: current resume (linked from the nav, hero, and contact section)
- `Raorane_Resume_EU.pdf`: EU-format resume (not currently linked)
- `og-image.png`: 1200x630 social/link preview image, matching the site's light theme. Referenced by the `og:image` and `twitter:image` meta tags.

## Theme

Single light theme. The color system is defined with CSS custom properties under `[data-theme="light"]` in `:root`; `<html>` is set to `data-theme="light"`.

## Local preview

Open `index.html` directly in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

Any static host works (GitHub Pages, Netlify, Cloudflare Pages, etc.); just push the folder, no build required. After deploying, set the canonical/live URL and confirm `og-image.png` is in place so shared links render a preview card.

## Accessibility & SEO

Includes a skip link, `prefers-reduced-motion` handling, semantic landmarks, JSON-LD `Person` structured data, and Open Graph / Twitter Card meta tags.
