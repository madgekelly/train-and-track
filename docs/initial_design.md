# Train & Track

## Overview
**Train & Track** is a simple, fast app to plan and log training and nutrition. 

The goal: quick logging, clear feedback, and no bloat.

---

## Problem

Existing workout trackers I have used are:

- Unintuitive
- Overly complex
- Slow to populate and prep

---

## Goals
**MVP:**

The first version will focus on training and workouts with meal
planning to come in a later iteration.

- Create programs and scheduled workouts.
- Log sessions quickly (sets, reps, weights, RPE, notes).
- See progress trends (PRs, volume, streaks).
- Sync via simple auth (email + password, JWT).

---

## Core User Stories
1. As a user, I can create a training programme.
2. As a user, I can add workouts to a training programme.
3. As a user, I can log a session quickly from my phone.
4. As a user, I can reuse templates (e.g. 5x5 bench).
5. As a user, I can track progress in workouts and exercises over time.
6. As a user, I can edit mistakes after logging.

---

## UI / Information Architecture
- **Dashboard**: Today’s workout, streak, quick log.
- **Programs**: List → Program → Workout.
- **Log**: “Start Session”, log sets quickly, finish.
- **Progress**: PRs, charts (volume, est. 1RM).
- **Library**: Exercises, templates.
- **Account**: Profile, units, export.

---

## System Architecture
To get this app up and running initial the focus is development speed:
- **Frontend**: React + Vite, with [MSW](https://mswjs.io/) for mock APIs.
- **Backend**: FastAPI (async SQLAlchemy + Alembic + Postgres).
- **Contracts**: OpenAPI spec in `/contracts/` (generated from FastAPI).
- **Docker**: Compose setup for API, frontend, and DB.

---

## Testing
- **Unit**: service functions (volume calc, streaks).
- **Integration**: repository/database queries.
- **API**: TBC

---

## Deployment Plan
- **Dev**: Docker Compose (FastAPI, Postgres, optional frontend).
- **Secrets**: stored in `.env` (never committed).

---

## Milestones
1. UI scaffold + mocks (React + MSW)
2. Initial API implementation
3. Backend auth
4. Progress endpoints + charts
5. Local deployment working
