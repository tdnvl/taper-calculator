# Taper & Pass Calculator

A small, mobile-optimized web app with three tools: a taper calculator, a pass calculator, and a mm/inch converter.

## Live app

https://tdnvl.github.io/taper-calculator/

## Taper Calculator

Enter three measurements:

- **D** — major diameter (larger end)
- **d** — minor diameter (smaller end)
- **Length** — length of the taper

Toggle between units:

- **mm** — results show taper per mm and taper angle
- **inch thousandths** — results show taper per inch and taper angle

If the minor diameter is entered larger than the major diameter, a dialog asks if you want to flip the values. Say no and the minor diameter field turns red instead.

### Formula

```
taper per unit = (D - d) / length
angle (degrees) = atan((D - d) / length / 2) × (180 / π)
```

## Pass Calculator

Enter target diameter and current diameter. Each has two boxes, mm or inch (three decimals). Fill one or the other, not both, the app clears the second box automatically.

The result shows how much material to remove or add:

- Big number: difference in thousandths of an inch
- Smaller, lower-contrast number below: same difference in mm
- Label above the number: Remove, Add, or On target

### Formula

```
diff (mm) = current diameter - target diameter
diff (thou) = (diff (mm) / 25.4) × 1000
```

## mm ⇄ in Converter

Type in either the mm or inch field and the other updates in real time. Each field has a copy button below it to grab that value for pasting into another calculator.

### Formula

```
inches = mm / 25.4
mm = inches × 25.4
```

## Navigation

Tap the hamburger icon (top right) to switch between the three tools. Pass Calculator is the default view on load.
