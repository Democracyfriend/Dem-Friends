# Democracy Friends polling poster generator

This repository includes a Python script that renders a high-contrast, blue-glow, Peter Max-inspired election poster JPG matching the Democracy Friends style shown in your mockup.

## Features
- Deep blue cinematic background with abstract paint-splash accents
- Ribbon banner and giant headline typography
- No candidate portraits
- Glowing bar chart with blue/red candidate segments
- Footer metrics block and source line
- JPG export for reports

## Quick start

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python scripts/democracy_friends_report.py --input examples/sample_poll_data.json --output examples/output/alaska_senate_report.jpg
```

## Files
- `scripts/democracy_friends_report.py` — poster generator
- `examples/sample_poll_data.json` — sample Alaska Senate poll input
- `examples/output/` — generated JPG is written here

## Example data format

```json
{
  "state": "ALASKA",
  "race": "U.S. SENATE RACE",
  "election": "GENERAL ELECTION 2026",
  "trend_label": "30-DAY TREND (LATEST)",
  "polling": [
    {
      "candidate": "MARY PELTOLA",
      "party": "Democrat",
      "value": 55.5,
      "color": [73, 168, 255],
      "portrait": null
    },
    {
      "candidate": "DAN SULLIVAN",
      "party": "Republican",
      "value": 45.6,
      "color": [228, 64, 64],
      "portrait": null
    }
  ],
  "source": "Gallup Polling",
  "margin_of_error": 3,
  "subtitle": "Strength In Numbers/Verasight (monthly polls)"
}
```
