# tryomarchy.com

Landing page for [Try Omarchy for Windows](https://github.com/tsouth89/try-omarchy-windows).
Static HTML, no build step, no JS, no trackers.

## Deployed

Live at https://tryomarchy.com (also on www). Cloudflare Pages project
`tryomarchy`, git-connected to this repo on `main` — every push to main
deploys automatically. Custom domains and certs are active.

## Assets still to add

- Real capture in the hero frame (see the HTML comment at the media slot):
  15-30s loop of theme switch / Super+Space menu / screensaver, captured with
  Windows tooling (Win+Shift+S or Xbox Game Bar; QMP screendump does not work on the GL path)
- Swap `og.png` for a version with a real screenshot when one exists

## Regenerating og.png

Made with ImageMagick, fonts are Noto Sans / Noto Sans Mono.
