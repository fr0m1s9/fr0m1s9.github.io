# Chirpy admin setup (Decap CMS)

This change adds a browser-based post editor at /admin/ without replacing the existing Chirpy theme or posts.

## What is included
- /admin/ Decap CMS entry point
- GitHub backend targeting fr0m1s9/fr0m1s9.github.io on master
- Post CRUD, per-post category/tag fields, and media uploads under assets/img/posts
- Existing GitHub Actions deploy remains unchanged

## Required before production
GitHub Pages cannot protect an OAuth client secret or run an OAuth callback server. An external, trusted OAuth backend is required. The placeholder `base_url` in `admin/config.yml` MUST be replaced before login works.

1. Deploy a vetted GitHub OAuth proxy (such as a reviewed Cloudflare Worker implementation). Inspect its code, redirect origins, state validation, CSRF protection, scopes, and token handling before deploying.
2. Create a GitHub OAuth App. Configure its callback URL to match that proxy's documentation.
3. Store the OAuth client secret only in the proxy's server-side secrets, never in this public repo.
4. Change `backend.base_url` to the deployed HTTPS endpoint and validate `auth_endpoint`.
5. Test login, post creation, editing, deletion, category/tag front matter, image URLs and the Pages workflow.

Only GitHub users with write access to this repository can publish.

## Notes
- Posts are Markdown under `_posts` with YAML front matter.
- Categories are edited per post. Renaming a category across all old posts is NOT implemented.
- The editor saves directly to `master` and triggers the existing `.github/workflows/pages-deploy.yml` workflow.
- Avoid merging this PR until an OAuth proxy is configured and basic validation succeeds.
