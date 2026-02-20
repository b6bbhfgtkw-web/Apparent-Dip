# Apparent Dip Calculator (Strike/Dip → Apparent Dip)

A simple, mobile-friendly calculator for **apparent dip** along a chosen **bearing/section direction**, built for structural geology / field methods.

This tool supports **two common field conventions** for plane attitude:
- **Azimuth (RHR)**: strike azimuth + true dip
- **Quadrant strike + dip direction**: strike in quadrant notation, plus dip and dip direction

> Designed to be easy for students to use on phones in the field and in labs.

---

## Features

- **Apparent dip** from true dip + strike + bearing (section direction).
- **Two input modes**:
  1. **Azimuth (Right-Hand Rule)**  
     - Input strike azimuth (0–360) and true dip (0–90)
     - Tool displays derived dip direction (strike + 90°)
  2. **Quadrant strike + dip direction**  
     - Strike examples: `N67E`, `S12W`, `NE`, `SW`, or numeric azimuth
     - Dip direction examples: `SE`, `S23E`, or `135`
     - Includes a **consistency check** (dip direction should be ~perpendicular to strike)

- Clean UI for use on phones/tablets/desktop.

---

## How the math works

The calculator uses the standard relationship:

**tan(apparent dip) = tan(true dip) × sin(θ)**

Where **θ** is the acute angle (0–90°) between the **strike line** and the **bearing/section direction**.

---

## Inputs

### Bearing / section direction (required)
- **Azimuth** (0–360°): the direction you want the apparent dip measured along (e.g., the trend of a cross section).

### Plane attitude (choose one)
**A) Azimuth (RHR)**
- Strike azimuth (0–360°)
- True dip (0–90°)

**B) Quadrant strike + dip direction**
- Strike (quadrant or azimuth)
- True dip (0–90°)
- Dip direction (quadrant or azimuth)

Accepted quadrant examples:
- Strike: `N67E`, `N 67 E`, `S12W`, `NE`, `270`
- Dip direction: `SE`, `S23E`, `135`

---

## Run it locally (no hosting)

### On a computer
1. Download this repository (Code → Download ZIP) or clone it.
2. Open `index.html` in your browser.

### On an iPhone/iPad (local HTML)
1. Put the project folder in the **Files** app (On My iPhone or iCloud Drive).
2. Tap `index.html` to open it.

Note: iOS can open HTML files from the Files app, but **some “website-like” behaviors (especially multi-page linking or server-relative paths) can be unreliable** when opened purely as local files. This project is intentionally single-page to avoid those issues. [4](https://discussions.apple.com/thread/255549790)

---

## Publish as a GitHub Pages site (optional)

If you want students to access it via a URL:

1. Ensure `index.html` is in the repo root (or in the folder you choose as the Pages source). GitHub Pages uses `index.html` (or `index.md`/`README.md`) as an entry file. [1](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)  
2. Go to **Settings → Pages** and select **Deploy from a branch**, then choose the branch/folder and save. [2](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)  
3. Upload/update files via GitHub’s web UI: **Add file → Upload files → Commit changes**. [3](https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository)  

---

## File structure

- `index.html` — the calculator UI + logic
- `manifest.json` — included for install/hosting scenarios (optional)
- `sw.js` — minimal service worker (optional; mostly relevant when hosted)
- `icon-192.png`, `icon-512.png` — icons for web app manifest

---

## Suggested classroom use

- GEOL/Structural labs: cross-section construction, map interpretation, and “apparent dip vs true dip” practice.
- Quick field checks: verify apparent dip along traverse or measured section direction.

---

## License

Free to use or modify as needed

---

## Contact / Attribution

Created by **Dr. Daniel Imrecke** (UHCL) for instructional use in geology and environmental science courses.
``
