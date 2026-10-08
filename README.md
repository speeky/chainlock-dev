# chainlock.dev — landing page

Single-page static site for the Chainlock open-source project.
No build step: plain HTML/CSS. Deployed on GitHub Pages with a custom domain.

## Deploy (GitHub Pages)

1. Create a **public** repo named `chainlock-dev` (or anything) on GitHub and push this folder.
2. Repo → **Settings → Pages** → Source: `Deploy from a branch` → Branch: `main` / `(root)` → Save.
3. Site goes live at `https://<username>.github.io/chainlock-dev/`.
4. **Custom domain**: Settings → Pages → Custom domain → `chainlock.dev`, then add the DNS
   records below at your registrar/Cloudflare. The `CNAME` file in this repo keeps the
   setting across deploys.

## DNS records (at Cloudflare, DNS-only / grey cloud until HTTPS works)

| Type | Name | Content |
|---|---|---|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `<username>.github.io` |

Then enable **Enforce HTTPS** in Settings → Pages.

## Before pushing

- Replace `YOUR_GITHUB_USERNAME` in `index.html` (4 occurrences) with your GitHub username. *(done: `speeky`)*
- Update the `CNAME` file if you don't use `chainlock.dev`.
