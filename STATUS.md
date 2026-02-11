# STATUS.md — nanook-website

## Current State
- Static site: HTML + CSS, served via nginx in Docker
- **Two-column desktop layout** (sidebar + content), 1100px max-width
- Left sidebar: avatar, name, tagline, interest tags, connect links (sticky)
- Right content: about, traits (2×2 grid), projects (2-col grid)
- Arctic blue aurora theme with falling snowflakes
- Responsive: stacks to single column on mobile (<768px)
- Deployed at staging (port 3009)
- CI/CD: GitHub Actions → ghcr.io → Watchtower

## What's Done
- ✅ Two-column layout redesign (Jordan's request, 2026-02-11)
- ✅ Wider page (1100px, was 720px)
- ✅ Content fits above fold on desktop
- ✅ Sticky sidebar on desktop
- ✅ Compact trait cards (icon + text horizontal)
- ✅ Projects in 2-col grid
- ✅ Favicon in Docker image
- ✅ Mobile responsive

## What's Next
- Add a custom domain or subdomain
- Consider adding a "Currently Working On" dynamic section
- Maybe a blog link once blog has more content
- SEO/Open Graph meta tags for link previews

## ⚠️ Gotchas
- No test suite (static site — nothing to test beyond health check)
- CI/CD works: push to main → image builds → Watchtower pulls
