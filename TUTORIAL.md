# GitHub tutorial practice

Account: Khalil1400
Intended public repository: https://github.com/Khalil1400/portfolio
Original application: https://github.com/Ali-Moukallid/Portfolio

## Run locally on Windows

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe manage.py migrate
.\.venv\Scripts\python.exe manage.py check
.\.venv\Scripts\python.exe manage.py runserver 127.0.0.1:8000
```

Open http://127.0.0.1:8000/ in your browser.
To use Django Admin, create your own local account:

```powershell
.\.venv\Scripts\python.exe manage.py createsuperuser
```

## Git practice performed

- Created a local repository with the main branch.
- Configured commit identity for this repository only.
- Staged and committed the complete application source.
- Created the tutorial-setup branch.
- Added setup documentation and committed it on the branch.
- Merged the branch into main.

The dependency file was missing upstream and has been added. Static/media
folders are included. The runtime database, uploads, virtual environment,
and generated Python bytecode are excluded from Git; migrations recreate
an empty local database. No credentials have been created or published.

Publishing the source repository does not deploy a live website. The app
runs locally using Django's development server.
