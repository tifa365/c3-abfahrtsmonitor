# 39C3 Bahnhofstafel

CCC Congress schedule displayed in the classic German train station departure board style (Bahnhofstafel).

## Usage

Open `index.html` directly in a browser. No build steps required.

### URL Parameters

- `?only-day=<n>` - Show single day (0-indexed)
- `?only-track=<name>` - Filter by track (e.g., `SCI`, `Security`)
- `?only-room=<room>` - Filter by room (substring match)

Parameters can be combined: `?only-day=1&only-track=SEC`

## Data Mapping

| Bahnhofstafel | CCC Schedule |
|---------------|--------------|
| Zeit (Time) | Talk start time |
| Zugnummer (Train ID) | Track code + talk ID (e.g., "SCI 12345") |
| Nach (Destination) | Talk title |
| Sprecher/Raum (Via) | Speakers, room name, end time |
| Gleis (Platform) | Room abbreviation |

## Styling

Uses the classic blue/yellow train station departure board colors:
- Navy blue (#000080) background
- Yellow (#FFFF00) headers
- White text on blue for departures
- Blue text on white for time cells

## Data Source

Fetches live from: `https://api.events.ccc.de/congress/2025/schedule.json`
