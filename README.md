# Jospan Media

Static rebuild of the Google Sites page at `media.jospan.com`, hosted on GitHub Pages.

## Files

```
index.html   the whole site (one page, styles inline)
assets/      logo variants, banner image, favicons
CNAME        custom domain for GitHub Pages
.nojekyll    serve files as-is, skip Jekyll processing
```

## Publishing

1. Push this repo to GitHub.
2. **Settings → Pages → Source: Deploy from a branch**, branch `main`, folder `/ (root)`.
3. Under **Custom domain**, confirm `media.jospan.com` and tick **Enforce HTTPS**.
4. At your DNS provider, point `media` at GitHub Pages:

   | Type  | Name    | Value                  |
   |-------|---------|------------------------|
   | CNAME | `media` | `<user>.github.io.`    |

   Replace `<user>` with the GitHub account or org that owns this repo. This
   replaces the record currently pointing at Google Sites.

If you'd rather not use the custom domain yet, delete `CNAME` and the site
serves from `https://<user>.github.io/<repo>/`.

## The font

Headlines use **Kopik**, licensed through Adobe Fonts, loaded from the existing
web project kit `xwe4bpb` — the same kit the Google Sites version used.

Adobe Fonts kits only serve to domains on their allow-list, so in
[Adobe Fonts → Web Projects → `xwe4bpb`](https://fonts.adobe.com/my_fonts#web_projects-section)
add whichever domains this site will be served from:

- `media.jospan.com`
- `<user>.github.io`
- `localhost` (for local previews)

Kopik is an Adobe Fonts family and can't be self-hosted under its licence, so
the kit link has to stay. If it fails to load, text falls back to Trebuchet MS /
Avenir Next rather than breaking the layout.

## Content

| Piece            | Source                                             |
|------------------|----------------------------------------------------|
| Logo             | `jospan media color and bw.ai`, vector-rendered at 600dpi |
| Banner           | captured from the original theme header            |
| "Get Pranked"    | links to `https://lol.jospan.com`                  |
| Video            | YouTube `mi7-DgF7Jvk`, privacy-mode embed          |

## Editing

It's one HTML file — open `index.html` and edit the markup directly. Brand
colours live in the `:root` block at the top:

```css
--green: #73C055;
--blue:  #0078BF;
```
