# Yaktonian Equity
Static site with optional live saving.

## Run it
- GitHub Pages: push to a repo, Settings > Pages > deploy from branch (root).
- Cloudflare Pages: connect the repo, leave the build command empty, output directory `/`.
- Keep the `functions` folder at the repo root (Cloudflare uses it; GitHub ignores it).

## Live saving (Cloudflare only)
1. Cloudflare dashboard > Storage & Databases > KV > create a namespace (any name).
2. Your Pages project > Settings > Bindings > add KV namespace, variable name `YQ`, pick that namespace.
3. Settings > Variables and secrets > add `ADMIN_PASSWORD` with the password you want.
4. Redeploy. Open /admin.html, sign in, and every change saves straight to the live site.

Menu names may differ slightly in the dashboard.

## Without live saving (e.g. GitHub Pages)
Admin changes save in your browser only. Admin > Publish > Download data.js, replace
`assets/data.js` in the repo, and push.
