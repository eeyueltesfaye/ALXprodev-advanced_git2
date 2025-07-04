
# ALX Advanced Git Project

This project demonstrates advanced Git workflows using **GitFlow**, **Git hooks**, and collaborative branching strategies. It's designed as part of the ALX Software Engineering curriculum.

## Project Structure

- `feature/*`: For developing new features (e.g., login, signup).
- `release/*`: For preparing production-ready releases.
- `hotfix/*`: For quickly patching critical issues on production.
- `develop`: Integration branch for features before release.
- `main`: Production-ready code lives here.

## Tasks Covered

### 1. Feature Branching

- Created `feature/implement-login` from `develop`.
- Created `login-page/README.md` with placeholder content.
- Committed with message:  
  `feat: scaffolding login page`

### 2. Release Workflow

- Created `feature/implement-signup` and added `signup-page/README.md`.
- Merged both feature branches into `develop`.
- Created `release/1.0.0` branch from `develop`.
- Updated `signup-page/README.md` with data requirements.
- Merged `release/1.0.0` into both `main` and `develop`.
- Tagged the release with `v1.0.0`.

### 3. Git Hooks Automation

- Implemented **pre-commit** hook:  
  Checks if every top-level directory contains a `README.md` file before allowing commits.
- Implemented **post-merge** hook:  
  Logs merges into `merge-log.txt` if merge occurs on the `main` branch.

## Git Flow Initialization

Initialized GitFlow with:

```bash
git flow init
```

Branches configured:
- Production: `main`
- Development: `develop`

## How to Run Locally

```bash
git clone <your-repo-url>
cd <repo-name>
git flow init
```

## Notes

- Git hooks must be placed in the `.git/hooks/` directory and made executable.
- The `merge-log.txt` file is created automatically when merging into `main`.

## License

This project is part of the ALX curriculum and is for educational purposes.
```
