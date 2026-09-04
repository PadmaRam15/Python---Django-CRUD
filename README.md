# Django Task Manager (CRUD App)

A simple full-stack CRUD (Create, Read, Update, Delete) application built with Python and Django. Users can add, view, edit, and delete tasks through a clean web interface backed by SQLite.

## Features

- Create new tasks with a title, description, and completion status
- View all tasks in a sortable list (newest first)
- Edit existing tasks
- Delete tasks with a confirmation step
- Django admin panel for direct data management
- Built with Django's class-based generic views (`ListView`, `CreateView`, `UpdateView`, `DeleteView`)

## Tech Stack

- **Backend:** Python, Django
- **Database:** SQLite (default, zero setup)
- **Frontend:** Django Templates, Bootstrap 5
- **Forms:** Django `ModelForm` with built-in validation

## Project Structure

```
django_crud_tutorial/
├── config/                 # Project settings, root URLs
│   ├── settings.py
│   └── urls.py
├── tasks/                  # Main app
│   ├── models.py           # Task model
│   ├── views.py            # Class-based CRUD views
│   ├── forms.py            # TaskForm (ModelForm)
│   ├── urls.py             # App-level routes
│   ├── admin.py            # Admin panel registration
│   └── templates/tasks/    # HTML templates
│       ├── base.html
│       ├── task_list.html
│       ├── task_form.html
│       └── task_confirm_delete.html
└── manage.py
```

## Getting Started

### Prerequisites

- Python 3.10+

### Installation

1. Clone the repository
   ```bash
   git clone https://github.com/PadmaRam15/django-task-manager.git
   cd django-task-manager
   ```

2. Create and activate a virtual environment
   ```bash
   python -m venv venv
   # Windows
   venv\Scripts\activate
   # macOS/Linux
   source venv/bin/activate
   ```

3. Install dependencies
   ```bash
   pip install django
   ```

4. Apply migrations
   ```bash
   python manage.py migrate
   ```

5. (Optional) Create an admin user
   ```bash
   python manage.py createsuperuser
   ```

6. Run the development server
   ```bash
   python manage.py runserver
   ```

7. Open your browser at `http://127.0.0.1:8000/`

## Admin Panel

Visit `http://127.0.0.1:8000/admin/` and log in with your superuser credentials to manage tasks directly.

## Roadmap / Next Steps

- [ ] Add Django REST Framework endpoints for API access
- [ ] Add user authentication so tasks are scoped per user
- [ ] Add due dates and priority levels
- [ ] Deploy to a production host with PostgreSQL

## License

This project is open source and available for learning purposes.
