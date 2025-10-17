# ParkSpotter

ParkSpotter is a small Django-based web application to help track parking entries, receipts, and basic reports. This repository contains the Django project, apps for accounts, entries, and receipts, plus static assets and templates for a simple UI.

## Features

- User account management (login / registration)
- Create and manage parking entries
- Generate receipts
- Earnings reporting
- Simple, template-based UI with static assets included

## Tech stack

- Python 3.x
- Django (see `requirements.txt` for the exact version)
- SQLite (default development database)
- HTML/CSS/JavaScript for frontend (templates in `static/templates` and `static`)

## Prerequisites

- Python 3.8+ installed and on PATH
- Git (optional)

Note for Windows PowerShell users: If you run into an execution policy error when activating virtualenv, use the included alternative activation command or temporarily adjust the execution policy for the process:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope Process
```

## Quickstart (Windows PowerShell)

1. Open PowerShell and navigate to the project root (where `manage.py` is located):

```powershell
cd 'C:\Users\MAHIM\OneDrive\Desktop\ParkSpotter'
```

2. Create and activate a virtual environment:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
# If activation is blocked, use the batch activate (cmd) instead:
# .venv\Scripts\activate.bat
```

3. Install dependencies:

```powershell
pip install -r requirements.txt
```

4. Run migrations and create a superuser (optional):

```powershell
python manage.py migrate
python manage.py createsuperuser
```

5. Start the development server:

```powershell
python manage.py runserver
```

6. Open your browser at http://127.0.0.1:8000/ to view the site.

## Running tests

```powershell
python manage.py test
```

## Project layout (important files/folders)

- `manage.py` - Django management script
- `parkspotter/` - Django project settings and URLs
- `accounts/`, `newEntries/`, `receipts/` - Django apps
- `static/` - CSS, JS, and templates used by the frontend
- `db.sqlite3` - Default SQLite database used for development

## Static files

During development Django serves static files automatically when `DEBUG = True`. For production, collect static files with:

```powershell
python manage.py collectstatic
```

and configure your web server (nginx, Apache, etc.) to serve them.

## Environment & Configuration

- Settings are in `parkspotter/settings.py`. For production deployments, be sure to set `DEBUG = False`, provide a secure `SECRET_KEY`, and configure allowed hosts and a production-ready database.



## License

Add your license here (e.g., MIT, Apache-2.0). If you want, I can add a license file and a short summary.


