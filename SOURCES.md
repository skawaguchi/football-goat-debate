# SOURCES

This document catalogs the data sources used to build the GOAT Ledger comparison page.
It is intended as a living reference for the dataset and a starting point for future migration into structured data.

## Document metadata

- Compiled: 20 July 2026
- Page: `goat-comparison.html`
- Repo: `football-goat-debate`

## Data categories

### 1. Player career totals
- Lionel Messi
  - Goals: club + country totals as of July 2026
  - Assists: official recorded assists across club and international competitions
  - Appearances: matches played in official club and national team competition
  - Sources (examples): official club records, national team records, Opta/StatsPerform, ESPN, Transfermarkt, FIFA match reports

- Cristiano Ronaldo
  - Goals: club + country totals as of July 2026
  - Assists: estimated modern assist totals where available
  - Sources: official club records, national team records, UEFA, FIFA, reputable sports statistic databases

- Pelé
  - Goals: competitive official match totals as of historical records
  - Source note: 757 goals uses competitive match counts; higher totals often include friendlies/tours
  - Sources: RSSSF, FIFA archives, Santos FC history, CONMEBOL records, historical research sites

- Diego Maradona
  - Goals and appearances from official club and Argentina records
  - Sources: FIFA archives, Napoli/S.S.C. records, Argentine Football Association history, RSSSF

- Kylian Mbappé
  - Goals, assists, appearances current to July 2026
  - Sources: official PSG/France records, UEFA, FIFA, Ligue 1 and Champions League match reports

- Lamine Yamal
  - Stats and honours current to July 2026
  - Sources: official FC Barcelona and Spain national team records, UEFA Euro 2024 records, 2026 FIFA World Cup records

### 2. Honours, trophies, and awards
- Ballon d'Or counts
  - Official Ballon d'Or announcements and archives
- Champions League titles
  - UEFA official competition history
- World Cup titles and tournament awards
  - FIFA official tournament records
- Continental honours
  - Copa América, Euro, Nations League, Copa Libertadores, Olympic Gold medal records
  - Source: respective confederation and tournament official sites

### 3. Notes and special cases
- Older eras predate consistent assist tracking, so Pelé and Maradona are shown as `N/A` for assists.
- Pelé and Maradona did not compete for the Ballon d'Or under the old Europe-only eligibility rules, so zero Ballons is shown with a historical note.
- Ronaldo assist totals vary by database; the page uses a rounded mid-range figure.
- Active player totals are rounded where necessary to reflect ongoing seasons and week-to-week changes.

## Suggested reference fields for future structuring
For a React PWA or JSON source file, use this schema for each player:
- `name`
- `country`
- `age`
- `careerStart`
- `apps`
- `goals`
- `assists`
- `goalsPerGame`
- `honours`
- `notes`
- `sources`

## Future source additions
- `SOURCES.md` should grow with each new data update.
- Add explicit URLs and access dates for every claim before the next major revision.
- If the site is migrated to structured data, preserve the original source mapping in the new dataset.
