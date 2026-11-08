# MiHub.ai brand pack

Brand colors: **MiHub Blue #005CA5**, **MiHub Orange #FAA61A**, dark surface **#0B2340**.
The mark and "iHub" are unchanged from MiHub; ".ai" is new, drawn in the same 2.93-unit stroke as the existing letters.

## Where each file goes in Omni

| Omni setting | File | Notes |
|---|---|---|
| Settings › Theme › Application › Logo | `omni-upload/omni-logo-24x24.svg` (or `@4x.png`) | 24×24 square mark |
| … Logo (dark mode) | `omni-upload/omni-logo-24x24-dark.svg` | |
| Settings › Theme › Application › Wordmark | `omni-upload/omni-wordmark-100x24.svg` (or `@4x.png`) | 100×24 slot |
| … Wordmark (dark mode) | `omni-upload/omni-wordmark-100x24-dark.svg` | |
| AI Hub › General › Branding › Agent image | `omni-upload/ai-agent-avatar-128.png` | 128×128 PNG; `-plain` has no sparkle |
| Settings › Theme › Application › colors | Interactive #005CA5, accent #FAA61A | |

Omni loads these by URL, so they must be on a public HTTPS host. Example with GCS:

```bash
gsutil mb -l us gs://copart-mihub-brand
gsutil -m cp -r omni-upload logo icon favicon gs://copart-mihub-brand/
gsutil iam ch allUsers:objectViewer gs://copart-mihub-brand
# URL pattern: https://storage.googleapis.com/copart-mihub-brand/omni-upload/omni-wordmark-100x24.svg
```

## Other uses
- `logo/` full lockups (light, dark, mono) as SVG + 1600px PNG for decks, email, the legacy MiHub banner
- `icon/` mark only, 512px
- `favicon/` .ico, 16–512 PNG, apple-touch-icon, for the mihub.copart.ai landing/redirect page
