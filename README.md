# Activate Your Voice (Static + CMS)

This repo is a Jekyll site that can be hosted on GitHub Pages and edited in a browser with Decap CMS.

## Quick start
1. Push this repo to GitHub.
2. In GitHub, enable Pages for the `main` branch.
3. Visit `https://YOUR_USERNAME.github.io/activate-your-voice-website/`.

## Editing content (simple web UI)
We use Decap CMS at `/admin/`.

### Setup OAuth for Decap CMS (required)
Decap CMS needs an OAuth app to let editors log in with GitHub.

**Option A (recommended):** Deploy the free Decap OAuth server
- Deploy https://github.com/decaporg/decap-cms-oauth-provider to any host (Netlify, Render, Vercel).
- Get the deployed URL (e.g., `https://cms-auth.yourdomain.com`).
- Update [admin/config.yml](admin/config.yml) with:
  ```
  backend:
    name: github
    repo: 1ForeverHDTest/activate-your-voice-website
    branch: main
    base_url: https://cms-auth.yourdomain.com
    auth_endpoint: auth
  ```
- In GitHub, create an OAuth App:
  - Homepage URL: your site URL
  - Authorization callback URL: https://cms-auth.yourdomain.com/auth/callback

**Option B:** Use Netlify + Git Gateway instead of GitHub Pages (simpler for non‑technical editors).

## Calendly and forms
- Update the Calendly link in [contact/index.md](contact/index.md).
- Replace `YOUR_FORM_ID` in [contact/index.md](contact/index.md) with your Formspree ID.

## Content folders
- Team members: `_team/`
- Blog posts: `_blog/`
- Pages: `index.md`, `the-team/index.md`, `blog/index.md`, `contact/index.md`

## Images
Upload images via the CMS. They are stored in `assets/img`.
