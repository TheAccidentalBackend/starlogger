# STAR LOGGER

A guided case-logging tool for field technicians. It walks a technician
through a fixed **Modem Health Check** every time, then builds a clean,
notepad-style **STAR log** (Situatie · Testen · Actie · Resultaat) that can be
copied straight into the case system.

The goal: make the same checks routine for every tech — from starter to
oldskool — so nothing gets skipped, while saving typing time.

## Features

- **Guided, forced Modem Health Check** (7 steps, in order):
  1. Levels Summary (historiek) — max 6 dB fluctuation
  2. Down & Upstream signals — Rx -4..+17 dBmV, Tx 25..47 dBmV
  3. Status History — deregs
  4. Streetping (Spot Charts) — Aftakdoos vs MO
  5. Docsis 3.1 OFDM (downstream) — profile 3 (QAM2048), partial service, uncorrectables
  6. OFDM RXMER — MER ≥ 32.4
  7. OFDMA (upstream) — ranging state, partial service, profile 11/12/13
- Each check: OK/NOK or Ja/Nee, an info tooltip with the norm, and
  action hints on the problem path.
- Case branch after the modem block: **Internet / iDTV / Telephony**.
- Free-type **Actie** and **Resultaat** with quick snippet buttons.
- **Modemtest** helper: paste-and-align, or a quick Rx/Tx/Snr block.
- Live log preview, one-tap **copy**.
- Trilingual: **NL / FR / EN** — the log follows the chosen language.
- Works fully **offline**, single self-contained HTML file.
- Phone- and laptop-friendly, Unit-T styling.

## Usage

Open `index.html` in any modern browser. No build step, no server, no
dependencies. Progress is saved locally in the browser.

## Status

Early demo / foundation. Wording, norms and answer types are being refined.
