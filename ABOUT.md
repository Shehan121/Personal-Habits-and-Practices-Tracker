# About This Project

A small two-person Python project: a personal habit/practice tracker, split into a logging half and an analysis half, connected by one shared CSV file.

## The Idea

- One shared CSV log sits between the two halves — date, activity, amount/duration per row
- Person 1 writes to it (the Logger), Person 2 reads and makes sense of it (the Analyzer)
- No need to work in sync — the CSV is the handoff point
- Built around whatever either of us already tracks (e.g. guitar practice)

## Logger — automation/systems side

- CLI loop: add entry / view entries / quit
- Input validation (duration must be numeric, date defaults to today)
- Writes rows via Python's `csv` module
- Optional: delete-last-entry, auto-filled date via `datetime`

## Analyzer — DS/ML side

- Reads the CSV (`csv` → `pandas`)
- Computes stats: total time, weekly average, longest streak, most consistent day
- Plots with `matplotlib`: activity over time, by day of week
- Stretch goal: simple trend line / next-week forecast

## Learning Goals

- Logger: functions, loops, conditionals, file I/O, input handling
- Analyzer: reading/parsing data, aggregation, visualization
- Both: combining two independent tools into one small multi-file project (imports, modules)
