# Assignment Management System

A comprehensive web-based application for managing academic assignments, lectures, and student-teacher interactions built with Django.

## Author
**Nidhi Yadav**

## Project Status
🚧 **Under Development**

## Overview

The Assignment Management System is a Django-based web application designed to streamline the assignment submission process and enhance academic collaboration between students and teachers. The platform provides a centralized hub for managing assignments, sharing lecture videos, and facilitating student-teacher communication.

## Features

### Core Functionality
- **User Authentication**: Secure registration and login system for students
- **Assignment Management**: Create, view, and submit assignments with file attachments
- **Lecture Videos**: Categorized video lectures for enhanced learning
- **Profile Management**: Student profiles with course and semester information
- **Gallery**: Visual content sharing and display
- **Contact System**: Direct communication channel for queries and feedback

### Key Components
- **Student Portal**: 
  - View assigned tasks by course and semester
  - Submit assignments with remarks and file attachments
  - Track submission dates and marks
  - Access lecture videos by category
  
- **Teacher Features**:
  - Create and assign tasks to specific courses
  - Set deadlines and total marks
  - Review student submissions
  - Upload lecture content

- **Administrative Features**:
  - Manage user registrations
  - Organize lecture categories
  - Monitor assignment submissions
  - Handle contact inquiries

## Technology Stack

- **Backend Framework**: Django 3.2.4
- **Database**: SQLite3
- **Frontend**: 
  - HTML5 Templates
  - Bootstrap CSS Framework
  - JavaScript
- **Language**: Python 3.x
- **Architecture**: MVT (Model-View-Template) Pattern

## Project Structure

```
assignment-management/
├── Myproject/              # Main Django project configuration
│   ├── settings.py         # Project settings
│   ├── urls.py            # URL routing
│   ├── wsgi.py           # WSGI configuration
│   └── asgi.py           # ASGI configuration
├── user/                  # Main application module
│   ├── models.py         # Database models
│   ├── views.py          # View functions
│   ├── urls.py           # App-specific URLs
│   ├── admin.py          # Admin interface configuration
│   └── migrations/       # Database migrations
├── templates/            # HTML templates
│   ├── base.html        # Base template
│   └── user/            # User-specific templates
├── static/              # Static files
│   ├── css/             # Stylesheets
│   ├── js/              # JavaScript files
│   ├── images/          # Static images
│   ├── webfonts/        # Font files
│   ├── gallery/         # Gallery images (user uploads)
│   ├── profile/         # Profile pictures (user uploads)
│   ├── teacherpic/      # Teacher profile pictures (user uploads)
│   ├── testfile/        # Assignment files (user uploads)
│   ├── answerfile/      # Student submission files (user uploads)
│   └── vcategory/       # Video category images (user uploads)
├── .gitignore          # Git ignore file
├── db.sqlite3          # Database file
├── manage.py           # Django management script
└── README.md           # Project documentation
```

## Database Models

### Core Models
- **asregster**: Student registration and authentication
- **teacherreg**: Teacher profiles and information
- **assignnmenttbl**: Assignment details and metadata
- **studentanswer**: Student submissions and evaluations
- **lecturecat**: Lecture video categories
- **lecturevideo**: Video lecture information
- **ugallery**: Gallery content management
- **contactInfo**: Contact form submissions

## Installation

### Prerequisites
- Python 3.x
- pip (Python package manager)
- Virtual environment (recommended)

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd "Assignment Management/Project"
   ```

2. **Create virtual environment**
   ```bash
   python -m venv venv
   ```

3. **Activate virtual environment**
   - Windows:
     ```bash
     venv\Scripts\activate
     ```
   - Linux/Mac:
     ```bash
     source venv/bin/activate
     ```

4. **Install dependencies**
   ```bash
   pip install django==3.2.4
   pip install Pillow  # For image handling
   ```

5. **Run migrations**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

6. **Create superuser (optional)**
   ```bash
   python manage.py createsuperuser
   ```

7. **Run development server**
   ```bash
   python manage.py runserver
   ```

8. **Access the application**
   - Open browser and navigate to: `http://127.0.0.1:8000/`
   - Admin panel: `http://127.0.0.1:8000/admin/`

## Usage

### For Students
1. Register with course and semester details
2. Login using email and password
3. View assignments for your course
4. Submit assignments before deadline
5. Access lecture videos by category
6. Update profile information

### For Teachers
1. Access admin panel
2. Create new assignments
3. Set deadlines and marking criteria
4. Review student submissions
5. Upload lecture videos

## Development Notes

### Security Considerations
- **Important**: The current `SECRET_KEY` in settings.py should be changed for production
- `DEBUG` mode should be set to `False` in production
- Configure `ALLOWED_HOSTS` for production deployment
- Implement proper password hashing and validation
- Add CSRF protection for forms

### Future Enhancements
- Email notifications for assignment deadlines
- Real-time chat between students and teachers
- Assignment grading and feedback system
- Advanced search and filtering options
- Mobile responsive design improvements
- API integration for third-party services
- Bulk upload functionality for assignments
- Analytics dashboard for performance tracking
- Multi-language support
- Export functionality for grades and reports

## Contributing

As this project is under development, contributions are welcome. Please follow these steps:

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## Known Issues

- Profile picture upload requires proper media file configuration
- Session management needs enhancement
- Form validation requires additional client-side checks
- Mobile responsiveness needs improvement

## Support

For issues, questions, or suggestions, please contact the author or create an issue in the project repository.

## License

This project is currently under development. License information will be added upon completion.

## Acknowledgments

- Django framework community
- Bootstrap for UI components
- Contributors and testers

---

**Note**: This is a development version. Do not use in production without proper security audits and testing.