# PaperTrail

PaperTrail is a browser history extractor designed specifically for [Comick.io](https://comick.io).  
It scans your browsing history across supported browsers, finds all visited comic pages, and organizes them into a structured SQLite database that shows your latest progress for each series.

---

## Features
- Detects all visited `https://comick.io/comic/...` pages
- Parses chapter and volume numbers (e.g. `ch001`, `v001`)
- Tracks the **latest chapter/volume read** for each series
- Saves results in a SQLite database:
  - One record per series
  - Includes series identifier (URL slug), latest chapter/volume, and source browser profile
- Output file is timestamped (`PaperTrail_YYYY-MMM-DD_HH-MM-SS.sqlite`)
- Works with multiple browsers:
  - Firefox
  - Chrome
  - Edge
  - Brave
  - Opera

---

## Usage

### 1. Clone the repository
```bash
git clone https://github.com/your-username/PaperTrail.git
cd PaperTrail
