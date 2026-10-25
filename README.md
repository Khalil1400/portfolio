# Portfolio Website

A Django portfolio with a CV page, project showcase, and collaboration form. A CSC263 Git exercise by Khalil1400, based on [Ali-Moukallid/Portfolio](https://github.com/Ali-Moukallid/Portfolio).

## Features

- CV and current work pages
- Collaboration requests with form validation
- Django Admin, Bootstrap 5, and SQLite

## Run locally

Use Python 3.12 or newer. In PowerShell:

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
$env:DJANGO_DEBUG="True"
.\.venv\Scripts\python.exe manage.py migrate
.\.venv\Scripts\python.exe manage.py check
.\.venv\Scripts\python.exe manage.py createsuperuser
.\.venv\Scripts\python.exe manage.py runserver 127.0.0.1:8000
```

On macOS/Linux, use `export DJANGO_DEBUG=True` and your activated Python environment. Open [localhost:8000](http://127.0.0.1:8000/); Django Admin is at `/admin/`. See [TUTORIAL.md](TUTORIAL.md) for the Git exercise.

## Configuration and security

- Debug is disabled by default. Explicit local debug mode generates a temporary signing key; sessions reset on restart.
- Before deployment, set a new private `DJANGO_SECRET_KEY`, configure `DJANGO_ALLOWED_HOSTS`, and keep debug disabled. Generate a key locally with `python -c "import secrets; print(secrets.token_urlsafe(50))"`. Never reuse a key from Git history.
- Set process environment variables; this project does not load `.env` automatically. Keep secrets, databases, uploads, and virtual environments out of Git.
- The original `/admin-dashboard/` route lacks an authentication guard. This exercise is for local use; protect that route before deployment.
