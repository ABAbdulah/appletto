# Appletto — company website

One-page website for **APPLETTO (SMC-PRIVATE) LIMITED**, a software company building mobile apps for Android and iOS.

It is a single static file — [`index.html`](index.html) — with no build step, no dependencies and no framework. Open it in a browser to view it, edit it in any text editor, and host it anywhere that serves static files.

## Publishing it on GitHub Pages

1. Repo **Settings → Pages**
2. **Source:** Deploy from a branch
3. **Branch:** `main`, folder `/ (root)` → **Save**

The site goes live at `https://abAbdulah.github.io/appletto/` within a minute or two. To use a custom domain, add it under the same Pages screen and point the DNS at GitHub.

## Things to fill in

Everything below is placeholder content. Search `index.html` for the text and replace it.

| What | Find | Replace with |
| --- | --- | --- |
| App cards | `App One`, `App Two`, `App Three`, `App Four` | Real app names + descriptions from your Play Store listings |
| Play Store links | `play.google.com/store/apps/developer?id=Appletto` | Your developer page URL, or each app's own listing URL |
| Email | `hello@appletto.com` | Your real contact address (appears 4 times) |
| Stats | `8+`, `100K+`, `4.5★`, `2025` | Your real numbers — or delete the whole `<div class="stats">` block |
| Site URL | `https://appletto.com/` | Your domain, in the `canonical` and `og:url` tags |

Add or remove app cards by copying or deleting a whole `<article class="app rv">…</article>` block — the grid reflows on its own.

## Changing the look

The colours and spacing all live in the `:root` block at the top of the `<style>` tag:

```css
--accent:   #00e5a0;   /* primary green */
--accent-2: #5b8cff;   /* secondary blue */
--bg:       #0a0b10;   /* page background */
```

Change those three values and the whole page follows.

## Adding real app icons

Each card uses an inline SVG placeholder. To use a real icon, drop the image into an `assets/` folder and swap the icon block:

```html
<div class="app-icon"><img src="assets/app-one.png" alt="" style="width:100%;height:100%;border-radius:14px"></div>
```

512×512 PNG (the same file you uploaded to Play Console) works well.
