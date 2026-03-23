# DeviceIQ

Marketing / demo site for **DeviceIQ — Invisible Device Detection SaaS** (React + Vite + Tailwind).

## View the site online (no login for visitors)

This repo ships a **pre-built** static site in the [`docs/`](./docs/) folder for **[GitHub Pages](https://pages.github.com/)**. Visitors open a normal URL; they do **not** need a GitHub or Vercel account.

### One-time setup (repo owner)

1. On GitHub: **Settings → Pages**
2. Under **Build and deployment → Source**, choose **Deploy from a branch**
3. Branch: **main** (or your default branch), folder: **`/docs`**
4. Save

Your site will be available at:

**https://rsx247.github.io/DeviceIQ/**

*(If the repository is renamed or under an organization, replace `rsx247` / `DeviceIQ` in the URL.)*

### Rebuild `docs/` from the zip

The source archive is [`accurate-device-detection-saas.zip`](./accurate-device-detection-saas.zip).

```bash
rm -rf webapp-source && mkdir webapp-source && unzip accurate-device-detection-saas.zip -d webapp-source
cd webapp-source && npm ci && npm run build
cp dist/index.html ../docs/index.html
```

Then commit and push the updated `docs/index.html`.

## Other free static hosts (viewers don’t log in)

Upload the contents of `docs/` (or use the built `index.html` alone) to any static host, for example:

- **Cloudflare Pages** — drag-and-drop or Git connect
- **Netlify Drop** — drag-and-drop at [app.netlify.com/drop](https://app.netlify.com/drop)
- **Surge.sh** — `npx surge docs/` (CLI signup for deployer only)
