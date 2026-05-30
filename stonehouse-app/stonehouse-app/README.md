# Stonehouse Café — Digital Menu

A fully interactive, mobile-first digital menu for Stonehouse Café, Hillcrest.

## 🚀 Live Demo

Deploy instantly on GitHub Pages — see [Setup](#github-pages-setup) below.

## ✨ Features

- **Cover page** with branded landing screen
- **12 menu categories** — 150+ items across Breakfast, Waffles, Burgers, Cocktails, G&T, Wine, Beer, Coffee, Milkshakes, Sweets, Kids & Cold Drinks
- **Page-based navigation** — category grid → section → item
- **Add / remove items** with live quantity controls
- **Order page** with save form (name, table number, special requests)
- **Clear order** with confirmation guard
- **Printable receipt** with order number, line items, totals and customer details
- **Counter slip** — "Please take your order to the counter"
- **Live search** within each section
- **Fully responsive** — mobile, tablet, desktop
- **Zero dependencies** — pure HTML/CSS/JS, no build tools needed

## 📁 Project Structure

```
stonehouse-app/
├── index.html          # Complete single-file app
├── README.md           # This file
├── .nojekyll           # Required for GitHub Pages
└── .github/
    └── workflows/
        └── deploy.yml  # Auto-deploy to GitHub Pages
```

## 🛠 GitHub Pages Setup

### Option A — Automatic (recommended)

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set Source to **GitHub Actions**
4. Push any commit — it deploys automatically ✅

### Option B — Manual

1. Push to GitHub
2. Go to **Settings → Pages**
3. Set Source to **Deploy from a branch**
4. Select `main` branch, `/ (root)` folder
5. Save — live in ~60 seconds ✅

## 🖥 Run Locally

No build step needed — just open the file:

```bash
# Clone your repo
git clone https://github.com/YOUR_USERNAME/stonehouse-app.git
cd stonehouse-app

# Open directly
open index.html

# Or serve locally (optional)
npx serve .
# or
python3 -m http.server 8080
```

## 📦 Deploy to GitHub (first time)

```bash
cd stonehouse-app
git init
git add .
git commit -m "Initial commit — Stonehouse Café menu"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/stonehouse-app.git
git push -u origin main
```

Then enable GitHub Pages in repo settings.

## 🔧 Customisation

All menu data lives in the `SECTIONS` array in `index.html`. Each section follows this structure:

```js
{
  key: 'breakfast',
  name: 'Breakfast',
  icon: '🍳',
  desc: 'Served all day, every day',
  sub: [
    {
      label: 'Sub-section heading',  // or null
      items: [
        {
          id: 'b1',           // unique ID
          name: 'Café Breakfast',
          price: 80,
          desc: 'Description text.',
          tags: [],           // 'v', 'popular', 'spicy'
          note: 'Optional note shown in gold',
        }
      ]
    }
  ]
}
```

### Change colours

Edit the CSS variables at the top of `index.html`:

```css
:root {
  --gold:   #b8922a;   /* brand gold */
  --green:  #2c4a22;   /* action green */
  --ink:    #1a1612;   /* primary text */
  --bg:     #f7f4ef;   /* page background */
}
```

## 📱 Browser Support

Works in all modern browsers. No polyfills needed.

- Chrome / Edge 88+
- Firefox 85+
- Safari 14+
- Mobile Safari / Chrome Android

## 📄 Licence

MIT — free to use and modify.

---

*Built for Stonehouse Café, Hillcrest · Est. 2019 · #GoodForKids*
