# STAR LOGGER

A guided case-logging tool for field technicians. It walks a technician
through the same analysis every time and builds a clean, notepad-style
**STAR log** (Situatie · Testen · Actie · Resultaat) that can be copied
straight into the case system.

The goal: make the same checks routine for every tech — from starter to
oldskool — so nothing gets skipped, while saving typing time.

## How it works

Every case starts with a **mandatory Modem / RF Health Check**. The tech
cannot skip it — that is the point: the modem analysis becomes routine.
After the modem block, the tool branches to the relevant layer for the
case, and finishes with free-typed Action and Result.

### 1. Modem / RF Health Check (always, in order)
1. Levels Summary (historiek) — max 6 dB fluctuation
2. Down & Upstream signals — Rx -4..+17 dBmV, Tx 25..47 dBmV
3. Status History — deregs
4. Streetping (Spot Charts) — Aftakdoos vs MO
5. Docsis 3.1 OFDM (downstream) — profile 3 (QAM2048), partial service, uncorrectables
6. OFDM RXMER — MER ≥ 32.4
7. OFDMA (upstream) — ranging state, partial service, profile 11/12/13

### 2. Case branch (after the modem block)
- **Internet** — in-home setup: WiFi coverage, APs / pods, WiFi statistics
  (SPOT / Plume Frontline), sticky & roaming clients, own hardware,
  interference.
- **iDTV** — STB checks: coax & connections, service menu 120 MHz, IP check,
  BER.
- **Telephony** — provisioning, test-phone dial tone & outgoing call
  (internal wiring is out of scope).

### 3. Action & Result
Free-typed, with quick snippet buttons and a **Modemtest** helper
(paste-and-align, or a quick Rx/Tx/Snr block).

## Features

- Guided, forced flow that writes the log as the tech answers.
- Per-check **OK/NOK** or **Ja/Nee**, an info tooltip with the norm, and
  action hints on the problem path.
- Live log preview, one-tap **copy**.
- Trilingual: **NL / FR / EN** — the log follows the chosen language.
- Works fully **offline**, single self-contained HTML file.
- Phone- and laptop-friendly, Unit-T styling.

## Usage

Open `index.html` in any modern browser. No build step, no server, no
dependencies. Progress is saved locally in the browser.

## Roadmap

- Refine wording, norms and answer types per check.
- Expand the in-home / WiFi analysis (Frontline & SPOT detail).
- More layers and case types over time.

## Status

Early demo / foundation — actively being refined.
