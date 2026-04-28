# 🌐 Website Components

Futuristic dark-mode UI components built for [mckee2success.com](https://mckee2success.com), embedded into Wix via HTML iFrame widgets.

---

## Files

| File | Description |
|------|-------------|
| `matrix-rain.html` | Animated green matrix rain canvas background |
| `glassmorphism-cards.html` | Frosted glass service cards with hover effects |
| `hero-section.html` | Full dark-mode hero section with animated headline and CTA |

---

## How to Embed in Wix

1. In Wix Editor, add an **HTML iFrame** element to your page
2. Click **"Enter Code"**
3. Paste the full contents of the relevant `.html` file
4. Resize the iFrame to fit your layout
5. Publish

> **Tip:** Each file is fully self-contained (no external dependencies) so it works out of the box in any iFrame.

---

## Component Details

### `matrix-rain.html`
- Full-canvas animated matrix character rain
- Color: `#00FF41` (classic matrix green)
- Transparent/dark background — works behind other elements
- Canvas auto-resizes to iFrame dimensions

### `glassmorphism-cards.html`
- Service cards with `backdrop-filter: blur()` frosted glass effect
- Hover lift animation
- Displays: Cybersecurity Consulting, GovCon Support, Cloud Security, GRC/Compliance
- Responsive 2×2 grid layout

### `hero-section.html`
- Full-width dark hero with animated text headline
- Tagline + call-to-action button
- Gradient background: deep navy → midnight black
- Font: Inter / system-ui

---

## Design System

| Token | Value |
|-------|-------|
| Primary Color | `#00FF41` (Matrix Green) |
| Background | `#0a0a0a` (Near Black) |
| Card Background | `rgba(255,255,255,0.05)` |
| Blur | `backdrop-filter: blur(12px)` |
| Border | `1px solid rgba(255,255,255,0.1)` |
| Font | Inter, system-ui, sans-serif |

---

## Notes

- All components are plain HTML/CSS/JS — no frameworks or build tools required
- Tested in Chrome, Firefox, and Wix's iFrame renderer
- For Wix embeds, keep file size lean — avoid importing external fonts or large libraries
- If the matrix rain is too CPU-heavy on mobile, reduce `fontSize` or increase `interval` in the script
