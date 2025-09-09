This project automates logging & reporting of daily fitness activities and generates:
- An **HTML Jinja2 dashboard** with per-person breakdowns and group totals.
- A **Markdown summary** with top performers and averages.
- **File automation**: archives generated outputs into a timestamped ZIP.
- **API Integration (optional)**: fetch records from a JSON API endpoint instead of a local file.

## Project Structure
```
fitness_activity_tracker_capstone/
├─ activities.json            # sample dataset 
├─ main.py                    # entry script
├─ templates/
│  └─ dashboard.html          # Jinja2 template
└─ (generated) build/
   ├─ report.html             # HTML dashboard
   ├─ summary.md              # Markdown summary
   └─ archive/report-*.zip    # archived copies
```
- Data & API: DJARIR MOHAMMED YACINE  
- Analytics & Python: KERFFAL SAMY  
- Templating & UI: TICHERAFI CAMELIA  
- Docs & Presentation: BENSAKAR OUSSAMA

