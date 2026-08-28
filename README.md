# tryomarchy.com

Landing page for [Try Omarchy for Windows](https://github.com/tsouth89/try-omarchy-windows).
Static HTML, no build step, no JS, no trackers.

## Deploy (Cloudflare Pages)

1. Cloudflare dashboard > Workers & Pages > Create > Pages > Connect to Git
2. Pick this repo (`tsouth89/tryomarchy-site`), branch `main`
3. Build settings: framework preset **None**, build command **(empty)**, output directory **/**
4. Project name: `tryomarchy` (gives you `tryomarchy.pages.dev`)

## Custom domain

If the tryomarchy.com zone is already on Cloudflare:

- Pages project > Custom domains > Set up a custom domain > `tryomarchy.com`
- Cloudflare creates the needed records automatically

If the zone is somewhere else, either move DNS to Cloudflare (free plan, recommended), or point these records at Cloudflare:

```
CNAME @    tryomarchy.pages.dev
CNAME www  tryomarchy.pages.dev
```

Apex CNAME flattening only works when the zone is on Cloudflare, so moving the zone is the clean path.

## Assets still to add

- Real capture in the hero frame (see the HTML comment at the media slot):
  15-30s loop of theme switch / Super+Space menu / screensaver, captured with
  Windows tooling (Win+Shift+S or Xbox Game Bar; QMP screendump does not work on the GL path)
- Swap `og.png` for a version with a real screenshot when one exists

## Regenerating og.png

Made with ImageMagick, fonts are Noto Sans / Noto Sans Mono.
