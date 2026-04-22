# Favicon Setup — sherylnexthome.com

## What to add to each page's <head>

```html
<!-- Favicon -->
<link rel="icon" type="image/png" href="/images/favicon-96x96.png" sizes="96x96" />
<link rel="icon" type="image/svg+xml" href="/images/favicon.svg" />
<link rel="shortcut icon" href="/images/favicon.ico" />
<link rel="apple-touch-icon" sizes="180x180" href="/images/apple-touch-icon.png" />
<meta name="apple-mobile-web-app-title" content="Ojai Homes" />
<link rel="manifest" href="/site.webmanifest" />
```

## site.webmanifest — create this file at repo root

```json
{
  "name": "Ojai Homes · Sheryl Whipple",
  "short_name": "Ojai Homes",
  "icons": [
    {
      "src": "/images/web-app-manifest-192x192.png",
      "sizes": "192x192",
      "type": "image/png",
      "purpose": "maskable"
    },
    {
      "src": "/images/web-app-manifest-512x512.png",
      "sizes": "512x512",
      "type": "image/png",
      "purpose": "maskable"
    }
  ],
  "theme_color": "#ffffff",
  "background_color": "#ffffff",
  "display": "browser"
}
```

## Recommended favicon generation

1. Start with a square source image — the NextHome "NH" mark or a clean "S" monogram works well
2. Go to **https://realfavicongenerator.net** (free)
3. Upload your source image
4. Download the package — it gives you all the files listed above at the right sizes
5. Drop the image files into `/images/` in the repo
6. Add `site.webmanifest` to the repo root
7. Add the `<head>` snippet to all 4 pages

## Quick option if you want something fast

If you don't have a ready logo file, the NextHome mascot (Luke) PNG already in the repo at
`/images/NH_Luke.png` could be cropped to square and used as a placeholder favicon while
a proper one is designed. Not ideal for brand consistency, but functional.
