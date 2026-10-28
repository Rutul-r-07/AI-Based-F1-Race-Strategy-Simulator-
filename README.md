# ApexMind — AI-Based F1 Race Strategy Simulator

ApexMind recommends Formula 1 tyre and pit-stop strategy from race
conditions — current lap, tyre compound and age, weather, safety-car
status, pit-stop time loss, and gaps to rivals — by combining four
classical AI techniques:

| Technique | What it does |
|---|---|
| **Forward Chaining** | Rule-based advisor — fires IF–THEN rules to flag conditions like high tyre wear or a weather mismatch |
| **CSP (Constraint Satisfaction)** | Generates and ranks feasible tyre-stint plans against tyre stock and regulations |
| **Minimax + Alpha-Beta pruning** | Evaluates the immediate pit-or-stay decision against a rival's likely response |
| **A\* search** | Finds the lowest-cost full-race sequence of stay/pit decisions |

All pace, degradation and pit-loss figures are simplified, illustrative
values — this is an educational simulator, not a predictor of real race
outcomes.

## Three ways to run it

| Build | File(s) | Run with |
|---|---|---|
| **CLI** | `apexmind.py` (single file) | `python3 apexmind.py --demo` or `python3 apexmind.py` |
| **Web app** | `apexmind_web/` (`backend.py` + `templates/` + `static/`) | `pip install flask` then `python3 backend.py`, open `http://127.0.0.1:5000` |
| **Standalone website** | `apexmind_website.html` (single file) | Just open it in any browser — no install, no server |

All three run the same four algorithms and produce matching results.
Pick whichever is easiest for your situation:
- No internet, nothing installed → **standalone website**
- Submitting for a lab/viva, need to show terminal output → **CLI**
- Want a dashboard with a form → **web app**

## Requirements

- Python 3.8+ (standard library only for the CLI and the core logic)
- Flask (only for the web app build — `pip install flask`)
- No requirements at all for the standalone website — just a browser

## Quick start

```bash
# CLI — instant demo run
python3 apexmind.py --demo

# Web app
cd apexmind_web
pip install flask
python3 backend.py
# then open http://127.0.0.1:5000

# Standalone website
# just double-click apexmind_website.html, or open it in a browser
```

## Notes

- No internet connection, API keys, or extra installs are required for
  the CLI or the website build.
- The web app's Flask server (`debug=True`) is meant for local use/demo,
  not public deployment as-is.
