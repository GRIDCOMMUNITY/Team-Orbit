# Local Route Finder

> Find the fastest, cheapest or simplest route across buses, ferries and walks.

Hack Day Haldia x GRID community - 6-hour build challenge

**Repo:** `team-orbit` | **Stack:** Python / Flask | **Difficulty:** Hard | **Time:** 6 hours

## Brief
Getting around a town means juggling buses, shared autos and ferries. Build a journey planner on a small transport network.

## Core tasks (must-do)
- [ ] Model a transport network: 15+ stops and 6+ routes with travel times and fares (SQLite or a seed file)
- [ ] Fastest path between two stops (Dijkstra)
- [ ] Switch the objective: fewest transfers or lowest fare
- [ ] Show up to 3 alternative routes
- [ ] UI: from / to with autocomplete, step-by-step journey, total time and fare
- [ ] Admin page to add stops and routes
- [ ] Handle 'no route found' gracefully

## Bonus tasks (only after the core works)
- [ ] Draw the route on a map (Leaflet)
- [ ] Timetable-aware 'next departure'
- [ ] Simulate a delay and re-route
- [ ] Natural-language query ('Stop A to Stop B after 6 pm') with an AI model

## What is already here
- `index.html` - base page that pings `/api/health`
- `app.py` - Flask app with a SQLite helper (`db()`, `init_db()`), `/api/health` and TODO endpoint stubs (they return 501 until you implement them)
- `requirements.txt` - `flask`, `gunicorn`

## Run locally
```bash
pip install -r requirements.txt
python app.py   # then open http://127.0.0.1:5000
```

## Deploy
Any Python host works (for example Render or PythonAnywhere). Start command: `gunicorn app:app`. Free hosts may reset the filesystem on restart, so the SQLite file can reset - fine for a demo.

## Suggested pacing
- Hour 1: read this README, agree on a plan and split the work
- Hours 2-4: build the core tasks
- Hour 5: integrate, polish, then bonus tasks if time allows
- Hour 6: deploy, open the Pull Request, submit on the MLH platform (OrganizerHQ)

## Submission checklist
- [ ] All core tasks work end to end
- [ ] Project is deployed and the live link opens
- [ ] Pull Request created on the Voyage GitHub repository assigned to your team
- [ ] Project submitted on the MLH platform (OrganizerHQ) - instructions are shared at the start of the event

## Rules
- Build new features on top of this starter project and integrate them.
- Teams of 3-4; every member must be present.
- AI tools and open-source / open-weight models are fully allowed.
