# tryomarchy.com

Landing page for [Try Omarchy for Windows](https://github.com/tsouth89/try-omarchy-windows).
Static HTML, no build step, no JS, no trackers.

## Deployed

Live at https://tryomarchy.pages.dev (production). Cloudflare Pages project:
`tryomarchy` (direct upload, not git-connected). To ship an update:

```bash
wrangler pages deploy . --project-name=tryomarchy --branch=main
```

Custom domains `tryomarchy.com` and `www.tryomarchy.com` are attached to the
Pages project; they finish activating once the DNS records below exist.

## DNS (pending, needs dashboard)

Zone `tryomarchy.com` is on Cloudflare. Neither the wrangler OAuth token nor
the Toolport Cloudflare token can write DNS records, so these two were left to
paste by hand (DNS > Records > Add record, both proxied):

```
CNAME @    tryomarchy.pages.dev
CNAME www  tryomarchy.pages.dev
```

## Assets still to add

- Real capture in the hero frame (see the HTML comment at the media slot):
  15-30s loop of theme switch / Super+Space menu / screensaver, captured with
  Windows tooling (Win+Shift+S or Xbox Game Bar; QMP screendump does not work on the GL path)
- Swap `og.png` for a version with a real screenshot when one exists

## Regenerating og.png

Made with ImageMagick, fonts are Noto Sans / Noto Sans Mono.
