# A kick-off project for python

# -Personal Habit/Practice Tracker-

A small CLI logger + a pandas/matplotlib analyzer, joined by one shared CSV.

## Authors

- **Hezz** — [Logger / Analyzer] — Information & Electrical Engineering @ HAW Hamburg
- **Shehan** — [Logger / Analyzer] — Software Design International @ TH Aschaffenburg

## Overview

- Tracks any recurring activity (practice, workouts, reading, etc.)
- Two independent tools, one shared data contract: `log.csv`
- Logger writes entries → Analyzer reads and visualizes them
- Later milestone: merge both into a single program

## Data Format

`log.csv` — one row per entry:

```
date,activity,amount
2026-09-11,guitar practice,30
```

## Getting Started

### Prerequisites

```bash
pip install pandas matplotlib
```

### Logger

```bash
python logger.py
```

- Menu loop: add entry / view entries / quit
- Duration must be numeric; date defaults to today if left blank

### Analyzer

```bash
python analyzer.py
```

- Reads `log.csv`
- Prints: total time, weekly average, longest streak, most consistent day
- Shows: line chart over time, bar chart by day of week

## Project Structure

```
habit-tracker/
├── logger.py        # Person 1 — CLI + CSV writer
├── analyzer.py       # Person 2 — pandas/matplotlib analysis
├── log.csv           # shared data file (generated)
├── README.md
└── ABOUT.md
```

## Roadmap

- [ ] Logger MVP (add / view / quit)
- [ ] Logger extras (delete last entry, auto date)
- [ ] Analyzer MVP (stats + 2 charts)
- [ ] Merge: Logger gets a `stats` command calling into `analyzer.py`
- [ ] Stretch: simple trend/forecast for next week

## Status

🚧 In progress
