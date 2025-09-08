# Learning Management System (LMS) - FSA Group 05

A comprehensive Django-based Learning Management System designed for educational institutions to manage courses, students, assessments, and learning analytics.

## 🚀 Features

### Core Features
- **User Management**: Student, instructor, and admin role management
- **Course Management**: Create, edit, and organize courses with modules
- **Assessment System**: Quizzes, assignments, and progress tracking
- **Learning Analytics**: Performance insights and progress reports
- **Collaboration Tools**: Forums, chat, and group collaboration
- **AI Integration**: AI-powered question generation and insights
- **Notification System**: Real-time progress notifications
- **Achievement System**: Badges and progress tracking

### Technical Features
- **Django 5.0.9** framework
- **SQLite/PostgreSQL** database support
- **Streamlit** integration for data visualization
- **AI/ML** capabilities with OpenAI and Google AI
- **Excel/Word** import/export functionality
- **Real-time** notifications and updates

## 📋 Prerequisites

- Python 3.11 or higher
- pip (Python package installer)
- Git

## 🛠️ Installation

### 1. Clone the Repository
```bash
git clone <repository-url>
cd FSA_Group05
```

### 2. Create Virtual Environment
```bash
python3 -m venv venv
```

### 3. Activate Virtual Environment

**On macOS/Linux:**
```bash
source venv/bin/activate
```

**On Windows:**
```bash
venv\Scripts\activate
```

### 4. Install Dependencies
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 5. Database Setup
```bash
python manage.py makemigrations
python manage.py migrate
```

### 6. Create Superuser (Optional)
```bash
python manage.py createsuperuser
```

**Alternative**: If you don't want to create a superuser, you can use the default admin account:
- **Username**: `tranleduy`
- **Password**: `tranleduy`

### 7. Run the Development Server
```bash
python manage.py runserver
```

The application will be available at `http://127.0.0.1:8000/`

## 📁 Project Structure

```
FSA_Group05/
├── LMS_SYSTEM/           # Main Django project settings
├── main/                 # Homepage and core functionality
├── user/                 # User management
├── course/               # Course management
├── quiz/                 # Quiz and assessment system
├── forum/                # Discussion forums
├── chat/                 # Real-time chat
├── analytics_report/     # Learning analytics
├── achievement/          # Achievement and badge system
├── progress_notification/ # Progress tracking
├── tools/                # Utility tools and data processing
├── static/               # Static files (CSS, JS, images)
├── media/                # User uploaded files
├── requirements.txt      # Python dependencies
└── README.md            # This file
```

## 🔧 Configuration

### Environment Variables
Create a `.env` file in the project root with the following variables:

```env
OPENAI_API_KEY=your_openai_api_key_here
SECRET_KEY=your_django_secret_key
DEBUG=True
```

### Database Configuration
The project is configured to use SQLite by default. To use PostgreSQL, update the database settings in `LMS_SYSTEM/settings.py`:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'your_database_name',
        'USER': 'your_username',
        'PASSWORD': 'your_password',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
```

## 🎯 Usage

### For Administrators
1. Access the admin panel at `http://127.0.0.1:8000/admin/`
2. Create user accounts and assign roles
3. Set up courses and modules
4. Configure system settings

### For Instructors
1. Log in with instructor credentials
2. Create and manage courses
3. Set up assessments and quizzes
4. Monitor student progress
5. Use AI tools for content generation

### For Students
1. Register or log in to the system
2. Browse available courses
3. Enroll in courses
4. Complete assignments and quizzes
5. Track learning progress
6. Participate in forums and discussions

## 🤖 AI Features

### Question Generation
- AI-powered quiz question generation
- Multiple question types support
- Content analysis and optimization

### Learning Analytics
- Performance insights
- Progress tracking
- Personalized recommendations

### Content Processing
- Excel/Word document processing
- Automated content extraction
- Data visualization tools

## 📊 Analytics and Reporting

The system provides comprehensive analytics including:
- Student performance metrics
- Course completion rates
- Learning path recommendations
- Progress visualization
- Custom report generation

## 🔒 Security Features

- User authentication and authorization
- Role-based access control
- CSRF protection
- Secure file uploads
- Data encryption

## 🚀 Deployment

### Production Deployment
1. Set `DEBUG = False` in settings
2. Configure production database
3. Set up static file serving
4. Configure email settings
5. Use a production WSGI server (e.g., Gunicorn)

### Docker Deployment (Optional)
```bash
docker build -t lms-system .
docker run -p 8000:8000 lms-system
```

## 🧪 Testing

Run the test suite:
```bash
python manage.py test
```

## 📝 API Documentation

The system includes RESTful APIs for:
- User management
- Course operations
- Assessment handling
- Analytics data retrieval

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests for new features
5. Submit a pull request

## 📞 Support

For support and questions:
- Create an issue in the repository
- Contact the development team
- Check the documentation

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Django framework
- Streamlit for data visualization
- OpenAI for AI capabilities
- All contributors and testers

## 📈 Roadmap

- [ ] Mobile app development
- [ ] Advanced AI features
- [ ] Multi-language support
- [ ] Enhanced analytics
- [ ] Integration with external LMS systems

---

**Note**: This is a development version. For production use, please ensure proper security configurations and testing.