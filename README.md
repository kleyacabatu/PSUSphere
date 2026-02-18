# PSUSphere

## Project Description

PSUSphere is a Django-based web application designed for managing student organizations and programs at Philippine State University (PSU). The system provides a centralized platform to organize and manage colleges, programs, organizations, students, and organization memberships.

## Features

- **College Management**: Create and manage colleges with automatic timestamp tracking (created_at, updated_at)
- **Program Administration**: Manage academic programs linked to specific colleges
- **Organization Directory**: Maintain a comprehensive list of student organizations with descriptions
- **Student Records**: Maintain student information including ID, name, and program affiliation
- **Organization Membership**: Track student membership in organizations with join dates
- **Advanced Admin Interface**:
  - Search functionality for colleges, programs, and organizations
  - Filtering capabilities by college and creation date
  - Display of related data across different entities
  - Clean list views with relevant information

## Technical Stack

- **Backend**: Django 6.0.2
- **Database**: SQLite
- **Python**: Python 3.x
- **Additional Libraries**:
  - ASGIREF 3.11.1
  - SQLParse 0.5.5
  - Faker 40.4.0 (for testing/data generation)

## Project Structure

```
PSUSphere/
├── projectsite/
│   ├── manage.py
│   ├── db.sqlite3
│   ├── projectsite/ (main Django project configuration)
│   └── studentorg/ (student organization app)
│       ├── models.py (College, Program, Organization, Student, OrgMember)
│       ├── admin.py (Django admin customizations)
│       └── ...
└── psusenv/ (virtual environment)
```

## Authors

- Kleya Roes (kleyaroes)

## Getting Started

1. Activate the virtual environment:
   ```
   source psusenv/Scripts/activate  # On macOS/Linux
   psusenv\Scripts\activate.bat     # On Windows
   ```

2. Run migrations:
   ```
   python manage.py migrate
   ```

3. Create a superuser for admin access:
   ```
   python manage.py createsuperuser
   ```

4. Start the development server:
   ```
   python manage.py runserver
   ```

5. Access the admin interface at `http://localhost:8000/admin/`
