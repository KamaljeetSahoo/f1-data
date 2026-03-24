# F1 Data

Static F1 race data served via GitHub Pages for the [f1-machine](https://github.com/KamaljeetSahoo/f1-machine) app.

## Structure

```
seasons/
  {year}/
    {round}-{location}/
      race/
        results.csv        # Final standings, grid, team, status, points
        laps.csv           # Every lap for every driver (sectors, tyres, speeds)
        weather.csv        # Air/track temp, humidity, wind, rainfall
        track_status.csv   # Green/yellow/SC/VSC/red flag changes
        race_control_messages.csv  # Steward messages, penalties
        session_info.json  # Total laps, driver list, start/end times
      qualifying/
      fp1/ fp2/ fp3/
      sprint/             # (2021+ sprint weekends only)
      event_info.json     # Event name, country, date, round

circuits/
  {location}.json          # Track geometry: 4000-point polyline + inner/outer edges
```

## Coverage

| Year | Rounds | Races | Sessions | Circuits |
|------|--------|-------|----------|----------|
| 2019 | 21 | 21 | 71+ | 21 |
| 2020 | 17 | 17 | 75+ | 17 |
| 2021 | 22 | 22 | 105+ | 22 |
| 2022 | 22 | 22 | 97+ | 22 |
| 2023 | 22 | 22 | 106+ | 22 |
| 2024 | 24 | 24 | 102+ | 24 |
| 2025 | 24 | 11* | 98+ | 24 |

*2025 season in progress

## Data Source

Extracted from [FastF1](https://github.com/theOehrly/Fast-F1) (telemetry-era: 2019+).

## Usage

Data is served at:
```
https://kamaljeetsahoo.github.io/f1-data/seasons/{year}/{round}-{location}/race/results.csv
https://kamaljeetsahoo.github.io/f1-data/circuits/{location}.json
```
