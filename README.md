# Democracy Friends Report Generator

This project generates a JPG report card for polling races in a stylized Democracy Friends / Peter Max-inspired format.

The design is data-driven so it can work for any state, race, and candidate set selected by the GUI or by a JSON input file.

## Requirements
- Python 3.9+
- Pillow

## Install
```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

## Run
```bash
python scripts/democracy_friends_report.py --input examples/sample_poll_data.json --output examples/output/alaska_senate_report.jpg
```

Windows Command Prompt:
```bat
python scripts\democracy_friends_report.py --input examples\sample_poll_data.json --output examples\output\alaska_senate_report.jpg
```

## JSON format
```json
{
  "state": "ALASKA",
  "race": "U.S. SENATE RACE",
  "election": "GENERAL ELECTION 2026",
  "trend_label": "30-DAY TREND (LATEST)",
  "title": "DEMOCRACY FRIENDS",
  "subtitle": "Real Polls / Real Data / A Stronger Democracy",
  "source": "Gallup Polling",
  "source_dates": "May 2025 - October 2026",
  "margin_of_error": 3,
  "polling": [
    {"candidate": "MARY PELTOLA", "party": "Democrat", "value": 55.5, "bar_color": [85, 180, 255]},
    {"candidate": "DAN SULLIVAN", "party": "Republican", "value": 45.6, "bar_color": [255, 82, 82]}
  ]
}
```

The renderer intentionally omits candidate portraits and instead emphasizes the bold poster look, glowing bars, deep-blue background, and abstract paint-splash styling.

