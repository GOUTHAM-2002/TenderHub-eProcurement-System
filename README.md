# 📋 TenderHub - Smart Tender Management System

**Digitize your tender process.** A complete web-based platform for managing government/private tenders, vendor registrations, bid submissions, and document workflows.

![Django](https://img.shields.io/badge/Django-4.0+-092E20?style=for-the-badge&logo=django&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-Database-003B57?style=for-the-badge&logo=sqlite&logoColor=white)

---

## 🎯 Overview

**TenderHub** streamlines the entire tender lifecycle from publication to vendor selection. Built for government departments, corporations, and procurement teams who need transparency, efficiency, and compliance.

**Real-world application:** Originally developed for Murdeshwar Temple administrative operations.

---

## ✨ Key Features

### 🏢 For Administrators
- **Publish tenders** with detailed requirements
- **Manage vendors** and their applications
- **Track submissions** in real-time
- **Document verification** and approval workflow
- **Compare bids** with analytics dashboard
- **Generate reports** (PDF, Excel)

### 👔 For Vendors
- **Register and create profile**
- **Browse active tenders**
- **Submit bids** with supporting documents
- **Track application status**
- **Upload certifications** (PAN, GST, licenses)
- **Receive notifications** for updates

### 🔒 Security & Compliance
- Role-based access control (Admin, Vendor, Auditor)
- Secure document upload and storage
- Audit trail for all actions
- Encryption for sensitive data

---

## 🚀 Quick Start

### Prerequisites
```bash
Python 3.8+
pip
virtualenv (recommended)
```

### Installation

1. **Clone the repository**
```bash
   git clone https://github.com/GOUTHAM-2002/TenderHub.git
   cd TenderHub
```

2. **Create virtual environment**
```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
   pip install -r requirements.txt
```

4. **Run migrations**
```bash
   python manage.py migrate
```

5. **Create superuser**
```bash
   python manage.py createsuperuser
```

6. **Run the server**
```bash
   python manage.py runserver
```

7. **Access the app**
   - Main app: `http://localhost:8000`
   - Admin panel: `http://localhost:8000/admin`

---

## 📂 Project Structure
```
TenderHub/
├── TenderManagement/     # Main Django project settings
├── tenders/              # Tender management app
│   ├── models.py        # Tender, Bid models
│   ├── views.py         # Business logic
│   ├── forms.py         # Form handling
│   └── templates/       # HTML templates
├── vendors/              # Vendor management app
│   ├── models.py        # Vendor profile
│   ├── views.py         # Vendor operations
│   └── templates/       # Vendor UI
├── documents/            # Document uploads
├── staticfiles/          # CSS, JS, images
├── db.sqlite3           # Database
├── manage.py            # Django CLI
└── requirements.txt     # Dependencies
```

---

## 🎨 Screenshots

> *Add screenshots here*

| Admin Dashboard | Vendor Portal | Bid Submission |
|----------------|---------------|----------------|
| ![Dashboard](screenshots/dashboard.png) | ![Vendor](screenshots/vendor.png) | ![Bid](screenshots/bid.png) |

---

## 🛠️ Tech Stack

- **Backend**: Django 4.0+
- **Database**: SQLite (easily upgradable to PostgreSQL)
- **Frontend**: HTML, CSS, JavaScript, Bootstrap
- **File Storage**: Local (configurable to S3/cloud)
- **Authentication**: Django's built-in auth system

---

## 📊 Database Schema

### Key Models

**Tender**
- Title, description, category
- Opening/closing dates
- Estimated budget
- Eligibility criteria
- Status (Draft, Published, Closed, Awarded)

**Vendor**
- Company name, contact info
- Registration documents (PAN, GST)
- Bank details
- Verification status

**Bid**
- Tender reference
- Vendor reference
- Quoted amount
- Technical/financial documents
- Submission timestamp

---

## 🔐 User Roles

| Role | Permissions |
|------|-------------|
| **Admin** | Create tenders, review bids, manage vendors, generate reports |
| **Vendor** | View tenders, submit bids, upload documents, track status |
| **Auditor** | View-only access to all tenders and bids |

---

## 💼 Workflow
```
1. Admin publishes tender
2. Vendors browse and apply
3. System accepts bids until deadline
4. Admin reviews submissions
5. Technical evaluation
6. Financial comparison
7. Award contract to winner
8. Generate work order
```

---

## 🌟 Features in Detail

### Admin Dashboard
- Overview of active/closed tenders
- Pending vendor approvals
- Recent bid submissions
- Quick actions and shortcuts

### Vendor Management
- Registration with document upload
- Profile verification workflow
- Rating and review system
- Blacklist functionality

### Tender Lifecycle
- Draft → Published → Open → Closed → Awarded
- Email notifications at each stage
- Automatic deadline enforcement
- Extension request handling

### Document Management
- Secure file uploads
- Format validation (PDF, DOC, XLS)
- Size limits and virus scanning
- Version control

---

## 🚀 Deployment

### Production Setup

1. **Update settings for production**
```python
   DEBUG = False
   ALLOWED_HOSTS = ['your-domain.com']
```

2. **Use PostgreSQL**
```bash
   pip install psycopg2
   # Update DATABASES in settings.py
```

3. **Collect static files**
```bash
   python manage.py collectstatic
```

4. **Deploy on**
   - **AWS/Azure/GCP**: Use EC2/App Service/Compute Engine
   - **Heroku**: `git push heroku main`
   - **DigitalOcean**: Deploy via App Platform
   - **PythonAnywhere**: Follow their Django guide

---

## 🔧 Configuration

### Email Settings
```python
# settings.py
EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
EMAIL_HOST = 'smtp.gmail.com'
EMAIL_PORT = 587
EMAIL_USE_TLS = True
EMAIL_HOST_USER = 'your-email@gmail.com'
EMAIL_HOST_PASSWORD = 'your-password'
```

### File Upload Settings
```python
MEDIA_URL = '/media/'
MEDIA_ROOT = os.path.join(BASE_DIR, 'media')
```

---

## 🧪 Testing
```bash
# Run tests
python manage.py test

# Check coverage
coverage run --source='.' manage.py test
coverage report
```

---

## 📈 Roadmap

- [ ] Multi-language support
- [ ] Mobile app (React Native)
- [ ] Blockchain integration for transparency
- [ ] AI-powered bid evaluation
- [ ] Integration with e-payment gateways
- [ ] Advanced analytics and reporting
- [ ] REST API for third-party integrations

---

## 🤝 Contributing

Contributions welcome! Please:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/Enhancement`)
3. Commit changes (`git commit -m 'Add enhancement'`)
4. Push to branch (`git push origin feature/Enhancement`)
5. Open a Pull Request

---

## 📄 License

This project is open source under the [MIT License](LICENSE).

---

## 👤 Author

**Goutham N**

- GitHub: [@GOUTHAM-2002](https://github.com/GOUTHAM-2002)
- Email: goutham3336@gmail.com
- LinkedIn: [Connect with me](https://www.linkedin.com/in/goutham-n/)

---

## 🙏 Acknowledgments

- Developed for **Murdeshwar Temple** administrative operations
- Inspired by government e-procurement systems
- Built with Django community support

---

## 📞 Support

For questions or support:
- Open an issue on GitHub
- Email: goutham3336@gmail.com
- Documentation: [Wiki](https://github.com/GOUTHAM-2002/TenderHub/wiki)

---

## 🌟 Show Your Support

If this project helped you or your organization:
- ⭐ Star this repository
- 🍴 Fork it for your use case
- 📢 Share with others who need tender management
- 💬 Provide feedback via issues

---

## 📊 Project Stats

![GitHub last commit](https://img.shields.io/github/last-commit/GOUTHAM-2002/TenderHub)
![GitHub issues](https://img.shields.io/github/issues/GOUTHAM-2002/TenderHub)
![GitHub pull requests](https://img.shields.io/github/issues-pr/GOUTHAM-2002/TenderHub)

---

**Built with 💼 for transparent procurement processes**

*"Bringing transparency and efficiency to tender management, one bid at a time."*
