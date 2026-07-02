# Taper Calculator

A small, mobile-optimized web app for calculating taper rate and angle. No build step, no dependencies. Just open `index.html` or visit the GitHub Pages link.

## Live app

https://YOUR-USERNAME.github.io/taper-calculator/

## What it does

Enter three measurements:

- **D** — major diameter (larger end)
- **d** — minor diameter (smaller end)
- **Length** — length of the taper

Toggle between units:

- **mm** — results show taper per mm and taper angle
- **inch thousandths** — results show taper per inch and taper angle

Fields use `inputmode="decimal"` so iOS shows the numeric keypad instead of the full keyboard.

## Formula

```
taper per unit = (D - d) / length
angle (degrees) = atan((D - d) / length / 2) × (180 / π)
```

## Local use

No install needed. Open `index.html` in any browser.

## Deploying updates

```bash
git add index.html
git commit -m "Update calculator"
git push
```

GitHub Pages rebuilds automatically after a push to `main`.
