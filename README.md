![CI Pipeline](https://github.com/sandeep9948/flask-docker-ci/actions/workflows/ci.yml/badge.svg)

# Dockerized Flask App with GitHub Actions CI

A minimal Python Flask application containerized with Docker. A GitHub Actions pipeline automatically builds the Docker image and validates the health endpoint on every push to main.

## Why I Built This
Containerization and CI pipelines are core DevOps skills. This project demonstrates building a Docker image and wiring it into an automated pipeline — the foundation of any modern delivery workflow.

## Project Structure

flask-docker-ci/
├── app.py              # Flask app with / and /health routes
├── Dockerfile          # Builds the container image
├── requirements.txt    # Python dependencies
└── .github/workflows/  # GitHub Actions CI pipeline

## CI Pipeline Steps
1. Checkout source code
2. Build Docker image
3. Start the container
4. Hit the /health endpoint — pipeline fails if it doesn't return 200

## Run Locally

```bash
docker build -t flask-app .
docker run -p 5000:5000 flask-app
```

Then open: http://localhost:5000/health
## Skills Shown
`Docker` `GitHub Actions` `CI/CD` `Python` `Flask` `Health Checks`
