# PaperTrail

Comick.io reading tracker across multiple browsers.

Purpose:
- Scan Firefox (and Gecko forks) and Chromium-based browsers (history + bookmarks).
- Find visited Comick.io comic pages (URLs under /comic/<slug>/...).
- For each comic (slug) keep one record and determine the latest chapter or volume visited
  (chapter -> stored as chNNN, volume -> vNNN).
- Export results to a timestamped SQLite file:
    Papers_YYYY-MMM-DD_HH-MM-SS.sqlite

Output schema (table `comics`):
  id | type | name | url | last_read | profile
  where:
    - type: History / Bookmark / TabStash
    - name: /<slug>/
    - url: a representative URL (the one that had the latest chapter)
    - last_read: e.g. ch010 or v001 (empty if not available)
    - profile: browser:profile label

Works on Windows, macOS, Linux. No external packages needed (Python 3.8+).
