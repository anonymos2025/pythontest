This project automates logging & reporting of daily fitness activities and generates:
- An **HTML Jinja2 dashboard** with per-person breakdowns and group totals.
- A **Markdown summary** with top performers and averages.
- **File automation**: archives generated outputs into a timestamped ZIP.
- **API Integration (optional)**: fetch records from a JSON API endpoint instead of a local file.

## Requirements Check (from assignment)
- Core Python: strings, integers/floats/booleans, conditionals, loops, lists & dicts ✅
- Modules: `json`, `os`, `datetime`, `requests`, `jinja2` ✅
- Templating: Jinja2 HTML template with a loop + conditional ✅
- Advanced feature: choose one → we included **API integration** (optional flag) **and** simple **file automation** ✅
- Deliverables: `main.py`, `README.md` ✅

## Project Structure
```
fitness_activity_tracker_capstone/
├─ activities.json            # sample dataset (28 records, mixed types; some missing calories)
├─ main.py                    # entry script
├─ templates/
│  └─ dashboard.html          # Jinja2 template
└─ (generated) build/
   ├─ report.html             # HTML dashboard
   ├─ summary.md              # Markdown summary
   └─ archive/report-*.zip    # archived copies
```

## Setup
1. Python 3.10+ recommended.
2. Install dependencies:
   ```bash
   pip install jinja2 requests
   ```

## Run (local file input)
```bash
cd fitness_activity_tracker_capstone
python main.py --outdir build
```

## Run (API mode)
Provide an endpoint that returns a JSON **list** of activity records with fields like:
`name, activity (RUN/BIKE/SWIM/GYM), duration (minutes), calories (optional), distance_km (optional), date (YYYY-MM-DD)`.

```bash
python main.py --use-api --api-url https://example.com/your-endpoint.json --outdir build
```

> The script tries to unwrap common wrapper keys (`data/items/records/result/value`) if the API returns an object.

## Notes
- The template contains conditionals to show `n/a` when calories are missing.
- The script warns if there are fewer than 20 records.
- You can edit `activities.json` freely or point `--input` to your own file.
- For presentation: open `build/report.html` in a browser and show the highlights from `summary.md`.

## Team Roles 
- Data & API: DJARIR MOHAMMED YACINE  
- Analytics & Python: KERFFAL SAMY  
- Templating & UI: TICHERAFI CAMELIA  
- Docs & Presentation: BENSAKAR OUSSAMA

