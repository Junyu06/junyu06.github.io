# Site Theme — Design System

This document defines the visual theme used across the site so that **all pages (Home, Resume, Contact, Experience, Education, Projects, and single project pages) stay consistent**. When adding or changing content or layouts, follow these rules.

---

## 1. Typography

### Fonts

| Use | Font | Weights | Source |
|-----|------|---------|--------|
| **Body, UI, narrative text** | **Space Grotesk** | 400, 500, 600 | Google Fonts |
| **Headings (h1–h6), mission, focus titles** | **Archivo** | 400, 500, 600, 700 | Google Fonts |

- Fonts are loaded globally in `layouts/partials/head.html` (Google Fonts).
- Fallback: `system-ui, sans-serif`.

### Usage in content

- **Home page** (`content/_index.md`): Uses classes `.mission`, `.narrative`, `.focus-heading`, `.area-block`, `.area-title`, `.area-desc`, `.nav-footer` — styles live in `layouts/index.html` (scoped to `.home-portal`).
- **All other pages**: Rely on global theme in `static/css/site-theme.css`. Wrap main content in **`.site-portal`** when using custom list/single layouts so typography and colors apply.

---

## 2. Colors

### Light mode

| Role | Hex | Usage |
|------|-----|--------|
| **Primary text (headings, strong)** | `#09090B` | h1–h6, titles, emphasis |
| **Body / secondary text** | `#3F3F46` | paragraphs, lists, descriptions |
| **Link hover** | `#2563EB` | underlined on hover |
| **Focus ring** | `#2563EB` | `:focus-visible` outline |

### Dark mode (`.dark` on `<html>`)

| Role | Hex | Usage |
|------|-----|--------|
| **Primary text** | `#fafafa` | headings, titles |
| **Body / secondary text** | `#a1a1aa` | paragraphs, lists |
| **Link hover** | `#60a5fa` | underlined on hover |
| **Focus ring** | `#60a5fa` | `:focus-visible` outline |

- Background and other UI (nav, buttons) stay with the theme (Paper theme + Tailwind). Only text and link colors are standardized here.

---

## 3. Links

- **Default**: Inherit text color, no underline.
- **Hover**: Underline + link color (`#2563EB` light / `#60a5fa` dark).
- **Focus**: 2px outline, offset 2px, same color as hover.
- **Motion**: `transition: color 0.2s ease, text-decoration-color 0.2s ease`. Disable with `@media (prefers-reduced-motion: reduce)`.

Apply to all in-content links (including in shortcodes) so they match the home portal nav-footer and prose links.

---

## 4. Layout & spacing

- **Content width**: Section and single-article content uses `max-width: 48rem` (e.g. `.site-portal section` in `site-theme.css`).
- **Vertical rhythm**: Section content uses `section > * + * { margin-top: 1.5rem }` (or equivalent) for consistent spacing between blocks.

---

## 5. Where theme is implemented

| File | Purpose |
|------|--------|
| `static/css/site-theme.css` | Global typography, colors, link styles, `.site-portal` section styles |
| `layouts/partials/head.html` | Loads Google Fonts (Archivo, Space Grotesk) + `site-theme.css` |
| `layouts/index.html` | Home-only styles (`.home-portal`) |
| `layouts/_default/list.html` | Section pages (Resume, Contact, etc.): `<article class="site-portal">` |
| `layouts/_default/single.html` | Single pages (e.g. project detail): `<article class="site-portal">` |

---

## 6. Adding new pages

1. **New section with only `_index.md`**  
   Rendered by `list.html`; already wrapped in `.site-portal`. No extra change.

2. **New single page (e.g. new project)**  
   Rendered by `single.html`; already wrapped in `.site-portal`. No extra change.

3. **New layout or custom template**  
   - Use **Space Grotesk** for body and **Archivo** for headings.
   - Use the colors in **§ 2** for text and link hover/focus.
   - Add `class="site-portal"` to the main content wrapper if you want the same section width and spacing.
   - Optionally reuse home-only classes (e.g. `.mission`, `.area-block`) only if you intentionally mirror the home structure; otherwise rely on `.site-portal` + `.prose`.

4. **New shortcodes or components**  
   - Use the same link and focus behavior as in `site-theme.css`.
   - Prefer semantic HTML and avoid hardcoded colors; theme CSS will apply.

---

## 7. Checklist for new or updated pages

- [ ] Headings use Archivo (handled by `.site-portal` / `.prose` in `site-theme.css`).
- [ ] Body text uses Space Grotesk and correct light/dark colors.
- [ ] Links have hover (underline + theme color) and visible focus ring.
- [ ] Content width is capped (e.g. 48rem) where appropriate.
- [ ] Reduced motion is respected for link transitions.

---

*Theme is aligned with the home page (home portal) and applied site-wide via `site-theme.css` and the layouts above. For UI/UX rules (icons, contrast, accessibility), see `.cursor/skills/ui-ux-pro-max/SKILL.md`.*
