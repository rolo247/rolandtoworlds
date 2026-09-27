# Roland to Worlds

Source for [RolandToWorlds.com](https://rolandtoworlds.com/), Roland's Road to the 2026 Powerlifting World Championships.

## Publishing

- Host: GitHub Pages for this repository; GitHub Actions builds and deploys on every push to `main` using `.github/workflows/deploy.yml`.
- Domain: `rolandtoworlds.com` is configured in repository Settings → Pages, with Enforce HTTPS enabled.
- DNS is managed at Porkbun: root ALIAS → `rolo247.github.io`; `www` CNAME → `rolo247.github.io`. Mail (MX/SPF) records are separate and must be preserved.
- AppDeploy was the former host and is no longer in the DNS path. Do not switch DNS back to `proxy-v2.appdeploy.ai` for ordinary site edits.

## Changing the site

- Edit page text and outgoing links in `index.html`, styling in `src/styles.css`, and photos in `public/resources/`.
- Commit changes to `main`. The deployment workflow runs automatically; check the Actions tab for a green run and then verify the live site, including photos and the GoFundMe, Bonfire, and sponsorship links.
- Local build check: `npm install` then `npm run build` (output in `dist/`).
- The ChatGPT GitHub connector supports reading this repository but does not grant write access. To make edits through ChatGPT Work, use an authenticated browser session; a normal Git client is another option.

## If the domain fails

1. Check the [GitHub Pages deployment workflow](https://github.com/rolo247/rolandtoworlds/actions) and [Pages settings](https://github.com/rolo247/rolandtoworlds/settings/pages).
2. Check the temporary Pages address: `https://rolo247.github.io/rolandtoworlds/`. With a custom domain configured, GitHub may redirect this address to the domain.
3. Check the root and `www` DNS records at Porkbun without changing the mail records. DNS caches can briefly keep an old destination after an edit.
4. After any fix, verify both `https://rolandtoworlds.com/` and `https://www.rolandtoworlds.com/` plus the campaign links before promoting the site.
