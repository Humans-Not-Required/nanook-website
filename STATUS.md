# STATUS.md — nanook-website

## Current State
- Static site: HTML + CSS, served via nginx in Docker
- **Two-column card layout** — visible card container with distinct sidebar
- Left sidebar: avatar, name, tagline, tags, links (darker background, ice-blue divider)
- Right content: about, traits (2×2 grid), projects (2-col grid)
- Arctic blue aurora theme with falling snowflakes, backdrop blur
- Wider layout: 92vw / 1300px max
- Responsive: stacks to single column on mobile (<768px)
- Favicon: SVG snowflake in browser tab
- Deployed at staging (port 3009), nanook.hnrstage.xyz
- CI/CD: GitHub Actions → ghcr.io → Watchtower

## What's Done
- ✅ Initial one-page website
- ✅ Two-column layout redesign (Jordan's request)
- ✅ Favicon in Docker image
- ✅ Open Graph + Twitter Card meta tags
- ✅ **Card container redesign (2026-02-12)**: main sits in visible card with background+border+rounded corners, sidebar has distinct darker bg, 2px ice-blue divider, wider 1300px layout, backdrop blur.
- ✅ **Comprehensive responsive design (2026-02-12)**: 4 breakpoints (1024/768/480/360px). Mobile: avatar+name side-by-side, full-width on small phones, safe-area insets for notched devices, 44px touch targets, trait grid 2×2→1col, project grid single-col on mobile.
- ✅ **Custom polar bear avatar (2026-02-12)**: Replaced generic DiceBear bottts SVG with hand-crafted polar bear face — glowing arctic-teal eyes, aurora backdrop, dark navy background, whisker dots, ambient sparkles. Matching simplified favicon. Reflects "Nanook" (Inuit for polar bear) identity.

## What's Next
- Add a custom domain or subdomain
- Consider adding a "Currently Working On" dynamic section
- Maybe a blog link once blog has more content

## ⚠️ Gotchas
- No test suite (static site — nothing to test beyond health check)
- CI/CD works: push to main → image builds → Watchtower pulls
