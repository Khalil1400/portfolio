# GitHub tutorial practice

CSC263 Git practice by Khalil1400. Based on [Ali-Moukallid/Portfolio](https://github.com/Ali-Moukallid/Portfolio).

## Run locally on Windows

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
$env:DJANGO_DEBUG="True"
.\.venv\Scripts\python.exe manage.py migrate
.\.venv\Scripts\python.exe manage.py check
.\.venv\Scripts\python.exe manage.py runserver 127.0.0.1:8000
```

Open http://127.0.0.1:8000/. Create your own local admin account with `.\.venv\Scripts\python.exe manage.py createsuperuser`. Local debug mode uses a temporary signing key; sessions reset on restart. See [README.md](README.md) for deployment environment settings.

## Git exercise

- Created a local repository and configured its commit identity.
- Committed the application source on main.
- Added setup documentation on tutorial-setup and merged it into main.
- Excluded runtime databases, uploads, virtual environments, bytecode, and private environment files.

Migrations recreate an empty local database. Publishing the source does not deploy a live website. Never reuse historical signing keys or commit private credentials.
