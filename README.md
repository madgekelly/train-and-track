# train-and-track
An app to track your workouts, meals, and macros. A CrossFit-inspired fitness and nutrition log built with Python.

# Repository Structure
```
train-and-track/
├── pyproject.toml
├── README.md
├── uv.lock
├── .gitignore
├── docker/
│   ├── .dockerignore
│   ├── Dockerfile
│   └── docker-compose.yaml
├── app/
│   ├── __init__.py
│   ├── main.py                 # FastAPI app factory & startup
```

# Local Development
Run the FastAPI backend with Docker Compose (using uvicorn under the hood):

```docker compose -f docker/docker-compose.yaml up --build```

Interactive Swagger UI →
http://localhost:8000/docs

Alternative ReDoc UI →
http://localhost:8000/redoc

Raw OpenAPI JSON schema →
http://localhost:8000/openapi.json

# Contributing

Commits follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
