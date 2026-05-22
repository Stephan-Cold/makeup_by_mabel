# Makeup By Mabel — Website Deployment Guide

## File Structure

```
/
├── index.html          ← The complete website
└── images/             ← Create this folder and add your images
    ├── hero.jpg        ← Hero/header background (1 image)
    ├── about.jpg       ← About section portrait (1 image)
    ├── gallery-01.jpg  ← Gallery image 1 (large feature)
    ├── gallery-02.jpg  ← Gallery image 2
    ├── gallery-03.jpg  ← Gallery image 3
    ├── gallery-04.jpg  ← Gallery image 4
    ├── gallery-05.jpg  ← Gallery image 5 (wide)
    ├── gallery-06.jpg  ← Gallery image 6
    ├── gallery-07.jpg  ← Gallery image 7
    ├── gallery-08.jpg  ← Gallery image 8
    ├── gallery-09.jpg  ← Gallery image 9 (wide)
    ├── gallery-10.jpg  ← Gallery image 10
    └── gallery-11.jpg  ← Gallery image 11
```

---

## Image Guidelines

### Hero (images/hero.jpg)
- **Purpose:** Full-screen cinematic background
- **Recommended size:** 1920×1080px minimum
- **Format:** WebP preferred, JPG accepted
- **Tip:** A close-up editorial portrait or dramatic beauty shot works best. Centre the focal point.

### About Portrait (images/about.jpg)
- **Purpose:** Mabel's professional portrait
- **Recommended size:** 800×1000px (portrait orientation)
- **Format:** WebP preferred, JPG accepted
- **Tip:** Good natural lighting, clean background, warm tones

### Gallery Images (images/gallery-01.jpg through gallery-11.jpg)
- **Purpose:** Portfolio showcase
- **Recommended size:** 800×1000px each
- **Format:** WebP preferred, JPG accepted
- **Tip:**
  - gallery-01.jpg is featured large (2×2 grid) — use your best/most dramatic look here
  - gallery-05.jpg and gallery-09.jpg span 2 columns — landscape-friendly shots work well
  - Keep filenames exactly as listed above

### Image Compression Tips
- Use [Squoosh](https://squoosh.app) or [TinyPNG](https://tinypng.com) to compress before uploading
- Aim for under 200KB per image
- WebP format is ~30% smaller than JPG at same quality

---

## Deployment

### Option 1: Simple File Hosting (Netlify, Vercel, GitHub Pages)
1. Create the `/images/` folder in the same directory as `index.html`
2. Add all 13 images with correct filenames
3. Upload the entire folder to your hosting platform
4. Done — no build step required

### Option 2: Spotify (as per brief)
> Note: If you mean a general web host rather than Spotify (which doesn't host websites),
> simply upload index.html and the /images/ folder to your host's root directory.

### Option 3: WordPress / Wix
- Upload index.html as a custom page template
- Place images in the `/images/` directory or update paths to match your CDN URLs

---

## Updating Image Paths

If your images are hosted at a CDN or different folder, find and replace all occurrences of:
```
src="images/
```
With your CDN path, e.g.:
```
src="https://cdn.yourhost.com/mabel/
```

---

## Customisation Quick Reference

| What to change | Where in the code |
|---|---|
| Phone number | Search `0846093357` — appears in 3 places |
| Operating hours | Search `08:00 – 17:00` |
| Service descriptions | Service card `<p class="service-desc">` blocks |
| Testimonials | `<article class="testimonial-card">` blocks |
| Stats (5+ years etc.) | `.stat-number` elements in the About section |
| Brand colour (rose) | CSS variable `--rose: #C9897A` |
| Footer copyright year | Bottom of `<footer>` |

---

## Performance Notes
- All gallery images load lazily (only when scrolled into view)
- No external JS libraries — pure vanilla JS
- Fonts load from Google Fonts with `display=swap` to prevent layout shift
- Total HTML file: ~77KB (images not included)

---

Built for Makeup By Mabel · Johannesburg, South Africa
