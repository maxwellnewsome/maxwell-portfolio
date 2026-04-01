# Maxwell Newsome — Portfolio

A dark, minimal personal portfolio site. Pure HTML/CSS/JS — no frameworks, no build step.

## Files

```
maxwell-portfolio/
├── index.html       ← All content lives here
├── style.css        ← All styles
├── script.js        ← Mobile nav + scroll animations
├── vercel.json      ← Vercel deployment config
└── README.md
```

## Editing content

Open `index.html` in VS Code. Everything is clearly commented by section:

- **Name / headline** → search for `Maxwell Newsome` and `Firmware & embedded`
- **About text** → find the `<section id="about">` block
- **Experience** → find `<section id="experience">` — copy/paste `.exp-item` blocks
- **Projects** → find `<section id="projects">` — copy/paste `.project-card` blocks
- **Skills** → find `<section id="skills">` — edit the `<span>` tags inside `.skill-tags`
- **Contact / links** → search `maxnew@student.ubc.ca`

## Adding your photo

1. Drop your photo into the project folder (e.g. `photo.jpg`)
2. In `index.html`, find the `<div class="about-img">` block
3. Replace the `<div class="about-img-placeholder">...</div>` with:
   ```html
   <img src="photo.jpg" alt="Maxwell Newsome">
   ```

## Adding your resume PDF

1. Drop `Maxwell_Newsome.pdf` into the project folder
2. The resume button in the About section already links to `Maxwell_Newsome.pdf` ✓

## Deploying to Vercel

### Option A — Vercel CLI (fastest)
```bash
npm i -g vercel
cd maxwell-portfolio
vercel
```
Follow the prompts. Your site will be live at a `.vercel.app` URL in ~30 seconds.

### Option B — Vercel Dashboard (no CLI needed)
1. Push this folder to a GitHub repo
2. Go to vercel.com → "Add New Project"
3. Import your GitHub repo
4. Framework preset: **Other** (it's a static site)
5. Click Deploy — done

### Custom domain
In the Vercel dashboard → your project → Settings → Domains → add your domain.

## Customizing colors

All colors are CSS variables at the top of `style.css`:

```css
:root {
  --accent: #b8a96a;   /* gold — headlines, labels */
  --accent2: #7aaa88;  /* green — company names */
  --link: #8aafc2;     /* blue — links */
  --text: #e5e1d8;     /* main text */
  --muted: #6b6760;    /* secondary text */
}
```
