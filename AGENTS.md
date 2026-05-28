# Moonglow GitHub Pages — Code Agent Guide

## Project Overview

This is a static website for the **Moonglow** App, hosted on **GitHub Pages**. It serves the following purposes:

- **Landing Page**: Product promotion and user onboarding
- **Privacy Policy**: Required for App Store / Google Play listing compliance
- **Terms of Service**: Required for legal compliance

## Tech Stack

| Item | Choice |
|------|--------|
| Hosting | GitHub Pages |
| Page type | Pure static HTML |
| CSS framework | Tailwind CSS v4 (CDN) |
| Scripting | No JS framework, vanilla only |
| Build tooling | None (zero build, deploy HTML directly) |

## Project Structure

```
moonglow/
├── index.html              # Home / Landing Page
├── privacy.html            # Privacy Policy (to be created)
├── terms.html              # Terms of Service (to be created)
├── AGENTS.md               # This file: Code Agent guide
└── CNAME                   # Custom domain config (if needed)
```

## Page Design Guidelines

### Visual Style
- **Primary color**: Deep night sky `#070a13`
- **Moonlight color**: Warm white / pale yellow `#fdf4d7`
- **Shadow side**: `#161b26`
- **Accent color**: Amber `amber-200/60`
- **Typography**: `font-mono` for headings, `font-sans` for body text
- **Language**: English (en)

### Design Principles
- Minimalist, clear information hierarchy
- Moon phase animation as the visual centerpiece
- Maintain a "quiet night" ambiance throughout
- Mobile-first, responsive layout

### Consistency Requirements
- All pages share the same `<head>` config (charset, viewport, Tailwind CDN, base styles)
- Footer consistently includes copyright info and navigation links
- Navigation: privacy / terms links placed in the footer
- Heading style reuses the H1 gradient style from `index.html`:
  ```html
  <h1 class="text-4xl md:text-5xl font-extrabold tracking-widest text-transparent bg-clip-text bg-gradient-to-b from-slate-100 to-slate-300 font-mono">...</h1>
  ```

## Deployment

This project is auto-deployed via GitHub Pages from the `main` branch. No build step required — push to deploy.

### Local Preview
```sh
# Any static server will work, e.g.:
python3 -m http.server 8080
# or
npx serve .
```

## Future Todos

- [ ] Create `privacy.html` — Privacy Policy page
- [ ] Create `terms.html` — Terms of Service page
- [ ] Add privacy/terms navigation links to `index.html` footer
- [ ] Consider adding a `CNAME` file for custom domain support
- [ ] Consider adding a `favicon.ico`
- [ ] Consider adding a `404.html` custom error page

## Notes

1. **Zero build deps**: All CSS via Tailwind CDN. Do not introduce npm / node_modules.
2. **Pure static**: No SSR or SSG frameworks.
3. **Use English**: All user-facing content in English. Code comments may be in English.
4. **Mobile-first**: All new pages must be mobile-responsive (use Tailwind responsive breakpoints like `md:`).
5. **Copyright year**: Remember to update the year in `© 2026 Moonglow` in the footer.