# PaperTrail

PaperTrail is a Comick.io reading tracker.  
It scans your browser history for comic pages, extracts the comic slug, and records the latest chapter or volume you’ve read. Results are saved to a timestamped SQLite database.

---

## Features
- Focused on **Comick.io** (`https://comick.io/comic/...`)
- Works across platforms: **Windows, Linux, macOS**
- Supports multiple browsers:
  - Firefox, Waterfox, LibreWolf, Pale Moon
  - Chrome, Edge, Brave, Opera, Vivaldi, Ungoogled-Chromium
- Detects and records:
  - Latest **chapter** read (`ch001`, `ch010`, etc.)
  - Latest **volume** read (`v001`, etc.)
- Deduplicates multiple visits into one record per comic
- Prioritizes **history** over bookmarks
- Exports results to a timestamped SQLite database:  
  `Papers_YYYY-MMM-DD_HH-MM-SS.sqlite`
- Prints a summary report of:
  - comics found
  - duplicates removed
  - unique entries saved

---

## Usage

### 1. Clone the repository
```bash
git clone https://github.com/your-username/PaperTrail.git
cd PaperTrail
