<p align="center">
  <img src="assets/pestable-logo.png" alt="Pestable" width="320">
</p>

<h1 align="center">Pestable — Pest Treatment Report App</h1>

<p align="center"><b>No pest, No stress.</b><br>
A single-file, mobile-first web app for pest control technicians to record jobs in the field
and generate a professional, branded <b>Pest Treatment &amp; Advice Report</b> (on-screen + PDF).</p>

---

## ✨ Overview

Pestable is **one self-contained `index.html` file** — HTML, CSS and JavaScript in a single
document. No install, no server, no login, no build step. Open it in any browser or add it to
your phone's home screen. All data stays **on the device** (browser `localStorage`).

## 🚀 Features

- **3-step guided record** — client & job → products → site & safety, with a progress indicator.
- **Auto-save drafts** — survives refreshes / accidental taps; resume from the dashboard.
- **Pests, areas inspected, treated areas, treatment methods, PPE** — quick tap-to-select.
- **Chemical product library** (15 common AU products pre-loaded, fully editable).
- **Amount Used dropdown** — 500 ml–50 L, blocks & dots, plus manual entry.
- **Address look-up** — free, keyless by default (OpenStreetMap / Nominatim); optional
  Geoapify API key for pinpoint house-number accuracy; manual typing always works.
- **Precautions** — generic pre-fill checkboxes + auto-fill from selected site risks.
- **Warranty dropdown** — Best effort · 30/60/90 days · 6 months · free text.
- **Site photos** — camera capture, auto-compressed, embedded in the report and PDF.
- **Weather at time of treatment** — auto-fetched (Open-Meteo) or entered manually.
- **Technician & client signatures** — drawn on-screen.
- **Search & "Repeat job"** — clone a previous report for recurring visits.
- **Backup & restore** — export/import all data as a JSON file.
- **Professional branded PDF** — real download via `html2pdf.js` (falls back to Print offline).

## 📱 Run it

**Locally:** download `index.html` and open it in any modern browser. On a phone, use
*Share → Add to Home Screen* for an app-like experience.

**Host it free on GitHub Pages:** see deployment below — the app then lives at a URL you can
bookmark on every technician's phone.

## 🌐 Deploy to GitHub Pages

1. Create a new GitHub repository and upload these files (keep `index.html` at the root).
2. In the repo: **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Select branch **`main`** and folder **`/ (root)`**, then **Save**.
5. Wait ~1 minute — your app is live at `https://<your-username>.github.io/<repo-name>/`.

## 🔌 Optional: better address accuracy

Address suggestions work out of the box with no key. For reliable **house-number** results,
grab a free [Geoapify](https://www.geoapify.com/) API key (≈3,000 lookups/day free) and paste
it into **Settings → Address Search** inside the app.

## 🛠 Tech

- Plain **HTML + CSS + JavaScript**, no framework, no build.
- `localStorage` for persistence (settings, reports, draft).
- External services are optional and only used online:
  [Open-Meteo](https://open-meteo.com/) (weather),
  [Nominatim](https://nominatim.org/) / [Geoapify](https://www.geoapify.com/) (address),
  [html2pdf.js](https://github.com/eKoopmans/html2pdf.js) via CDN (PDF export).

## 🔒 Privacy

No accounts, no analytics, no tracking. Records never leave the device except via the optional
weather/address look-ups and the PDF you export yourself. Because data is device-only, **export
a backup regularly** (Settings → Data & Backup).

## ⚠️ Note on bundled details

This build ships with **Pestable Pty Ltd** branding and contact details (already publicly listed
on the company website and ABN register). Edit them any time in **Settings**, or change the
`DEFAULT_DETAILS` / logo in `index.html` to rebrand for another business.

## 📄 License

Released under the [MIT License](LICENSE).
