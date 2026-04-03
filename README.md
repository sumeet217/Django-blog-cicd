# 📝 Simple Django Blog App

A clean, lightweight blog application built with **Django 6.0**. Users can browse all published posts on the home page and read individual posts on dedicated detail pages. Content is managed through the built-in Django admin panel.

---

## ✨ Features

- **Home Page** — Lists all blog posts in reverse chronological order with truncated previews
- **Post Detail Page** — Displays the full content of a selected blog post
- **Admin Panel** — Create, edit, and delete posts via Django's built-in admin interface
- **SQLite Database** — Zero-configuration database for local development

---

## 🛠 Tech Stack

| Layer      | Technology       |
| ---------- | ---------------- |
| Language   | Python 3.13+     |
| Framework  | Django 6.0.3     |
| Database   | SQLite 3         |
| Templating | Django Templates |
| Styling    | Inline CSS       |

---

## 📁 Project Structure

```
simple-django-blog-app/
├── blogs/                  # Django project configuration
│   ├── __init__.py
│   ├── asgi.py             # ASGI entry point
│   ├── settings.py         # Project settings
│   ├── urls.py             # Root URL configuration
│   └── wsgi.py             # WSGI entry point
│
├── posts/                  # Blog application
│   ├── __init__.py
│   ├── admin.py            # Admin registration for Post model
│   ├── apps.py             # App configuration
│   ├── migrations/         # Database migrations
│   ├── models.py           # Post data model
│   ├── tests.py            # Unit tests
│   ├── urls.py             # App-level URL routes
│   └── views.py            # View functions (index, post detail)
│
├── templates/              # HTML templates
│   ├── index.html          # Home page — lists all posts
│   └── posts.html          # Detail page — single post view
│
├── .gitignore
├── manage.py               # Django management script
├── requirements.txt        # Python dependencies
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

- **Python 3.13+** installed on your system

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/sumeet217/simple-django-blog-app.git
   cd simple-django-blog-app
   ```

2. **Create and activate a virtual environment**

   ```bash
   python3 -m venv venv
   source venv/bin/activate        # macOS / Linux
   venv\Scripts\activate           # Windows
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Run database migrations**

   ```bash
   python manage.py migrate
   ```

5. **Create an admin user** _(optional, for managing posts)_

   ```bash
   python manage.py createsuperuser
   ```

6. **Start the development server**

   ```bash
   python manage.py runserver
   ```

7. **Open in your browser**

   ```
   http://127.0.0.1:8000/
   ```

---

## 🔗 URL Routes

| Route            | View       | Description                    |
| ---------------- | ---------- | ------------------------------ |
| `/`              | `index`    | Home page — all posts          |
| `/post/<id>`     | `post`     | Detail page — single post      |
| `/admin/`        | _built-in_ | Django admin panel             |

---

## 📦 Data Model

### `Post`

| Field        | Type              | Description                          |
| ------------ | ----------------- | ------------------------------------ |
| `title`      | `CharField(255)`  | Title of the blog post               |
| `body`       | `CharField(1M)`   | Full body content of the post        |
| `created_at` | `DateTimeField`   | Timestamp when the post was created  |

---

## 📄 License

This project is open source and available for personal and educational use.
