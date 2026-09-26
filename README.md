# GitHub Actions + Docker CI/CD Project
A simple Node.js/Express app, containerized with Docker, automatically built
and pushed to Docker Hub via a GitHub Actions pipeline on every push to main.
## Architecture
GitHub push -> GitHub Actions -> docker build -> docker push -> Docker Hub
## Technologies Used- Node.js, Express- Docker (multi-layer caching optimized Dockerfile)- GitHub Actions (CI/CD)- Docker Hub (image registry)
## How to Run Locally
docker pull iamkartik2097/gha-docker-project:latest
docker run -d -p 3000:3000 iamkartik2097/gha-docker-project:latest
## Challenges I Faced- Ubuntu apt mirror errors installing Node.js (fixed with apt-get update, or
  installing via NodeSource)- GitHub no longer accepts account passwords for git push - needed a
  Personal Access Token (classic, with the "repo" scope)- Confused the GitHub PAT with the Docker Hub access token - they are two
  separate tokens for two separate systems- YAML: missing space after "push:" broke the whole workflow file- YAML: wrote "secrets/NAME" instead of the correct "secrets.NAME" (dot,
  not slash
