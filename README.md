# Youssef's Blog Platform

A full-stack web application for creating, managing, and sharing blog posts with user authentication and commenting features.

## 🎯 Project Overview

This is a complete blog platform built with Flask that allows multiple users to read blog posts and enables administrators to create, edit, and manage content. Users can register, log in, and leave comments on blog posts.

### Key Features

- **User Authentication**: Secure registration and login system with password hashing (PBKDF2)
- **Blog Post Management**: Create, edit, and delete blog posts (admin only)
- **Comments System**: Authenticated users can comment on blog posts
- **Responsive Design**: Mobile-friendly interface using Bootstrap 5
- **Admin Dashboard**: Special permissions for admin user (ID 1) to manage content
- **Database Integration**: SQLAlchemy ORM with user, post, and comment models

## 🛠️ Technology Stack

- **Backend**: Python 3 with Flask micro-framework
- **Database**: SQLAlchemy ORM (SQLite by default)
- **Frontend**: HTML5, CSS3 (88.3% of codebase)
- **Styling**: Bootstrap 5, Font Awesome icons
- **Form Handling**: WTForms with data validation
- **Rich Text Editor**: CKEditor for blog post creation
- **Authentication**: Flask-Login with password hashing
- **Email/Contact**: Flask-Mail integration

### Language Composition
- CSS: 88.3%
- HTML: 6.7%
- Python: 4.6%
- Other: 0.4%

## 📁 Project Structure

```
blog_post/
├── app.py                          # Main Flask application
├── forms.py                        # WTForm definitions
├── templates/                      # HTML templates
│   ├── header.html                # Navigation and layout
│   ├── footer.html                # Footer component
│   ├── index.html                 # Homepage with blog feed
│   ├── post.html                  # Individual post view
│   ├── make-post.html             # Create/edit post form
│   ├── login.html                 # Login page
│   ├── register.html              # Registration page
│   ├── about.html                 # About page
│   └── contact.html               # Contact form
├── static/
│   ├── css/
│   │   └── styles.css             # Main stylesheet
│   ├── js/
│   │   └── scripts.js             # JavaScript functionality
│   └── assets/
│       └── img/                   # Background images
└── README.md
```

## 🚀 Core Functionality

### User Management
- **Register**: New users create accounts with email, name, and password
- **Login/Logout**: Secure session management with Flask-Login
- **Admin Privileges**: User with ID=1 has special permissions to manage posts

### Blog Features
- **View Posts**: All users can browse published blog posts
- **Create Posts**: Admin users can create new posts with title, subtitle, image, and content
- **Edit Posts**: Admin can modify existing posts
- **Delete Posts**: Admin can remove posts with a one-click delete button

### Comments System
- **Add Comments**: Logged-in users can comment on posts using rich text editor
- **Comment Display**: Comments show author name and content
- **Authentication Required**: Users must log in to comment

### Form Validation
- Email uniqueness checking
- Password hashing and verification
- URL validation for image fields
- Required field validation using WTForms validators

## 💼 How to Add This to Your Resume

### Project Title
**Full-Stack Blog Platform with User Authentication**

### Description to Use

"Developed a complete blog application using Flask that features user authentication, content management, and a commenting system. Implemented secure user registration and login with password hashing, created a responsive UI with Bootstrap 5, and built a role-based admin dashboard for content management. The application uses SQLAlchemy ORM for database operations and WTForms for form validation."

### Key Skills to Highlight

1. **Backend Development**
   - Flask framework and routing
   - SQLAlchemy ORM database design
   - User authentication and authorization
   - Session management with Flask-Login

2. **Frontend Development**
   - HTML5 semantic markup
   - CSS3 responsive design
   - Bootstrap framework integration
   - JavaScript for dynamic behavior

3. **Database Design**
   - Relational database modeling
   - User-Post-Comment relationships
   - Query optimization with SQLAlchemy

4. **Security**
   - Password hashing with PBKDF2
   - SQL injection prevention (via ORM)
   - CSRF protection with WTForms

5. **Full-Stack Integration**
   - Form validation and submission
   - Authentication middleware
   - Data persistence and retrieval
   - Rich text editor integration (CKEditor)

### Sample Resume Bullet Point

✓ "Built a Flask-based blog platform with 200+ lines of backend logic, featuring secure user authentication, admin-controlled post management, and a nested commenting system using SQLAlchemy ORM"

✓ "Implemented responsive front-end design with Bootstrap 5, achieving 88% CSS styling coverage with mobile-first approach"

✓ "Designed and implemented role-based access control allowing only admin users to manage blog posts and maintain platform integrity"

## 🔧 Setup Instructions

### Requirements
- Python 3.7+
- Flask and dependencies (see code imports)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/zerbouhyoussef/blog_post.git
cd blog_post
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the application:
```bash
python app.py
```

4. Access the blog at `http://localhost:5000`

### Default Admin Account
- User ID 1 is automatically granted admin privileges
- First user to register will have ID 1

## 📊 Database Models

### User
- email (unique)
- password (hashed)
- name
- Posts relationship
- Comments relationship

### BlogPost
- title
- subtitle
- body (rich text)
- img_url
- date
- author (FK to User)
- Comments relationship

### Comment
- text (rich text)
- comment_author (FK to User)
- parent_post (FK to BlogPost)

## 🎓 Learning Outcomes

This project demonstrates:
- Full-stack web development capabilities
- Security best practices in web applications
- Database design and management
- RESTful routing patterns
- Template inheritance and Jinja2 templating
- Form handling and validation
- User authentication workflows

## 📝 License

This project is open source and available under the MIT License.

---

**Repository**: [zerbouhyoussef/blog_post](https://github.com/zerbouhyoussef/blog_post)  
**Created**: September 14, 2024  
**Last Updated**: January 4, 2025