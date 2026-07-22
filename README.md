# 🛍️ Velora

> A modern Django-based fashion e-commerce platform featuring product discovery, shopping cart management, secure authentication, order processing, and an administrative dashboard.

---

## 🚀 Project Overview

Velora is a full-featured fashion e-commerce application built with Django. It enables customers to browse products, manage shopping carts, place orders, and leave product reviews, while providing administrators with a secure dashboard to manage products, categories, inventory, and customer orders.

This project demonstrates practical implementation of Django concepts including:

- Model-driven architecture
- Authentication and authorization
- Database relationships using Django ORM
- Custom management commands
- Product filtering and searching
- Django Admin customization

---

## ✨ Features

### Customer Features

- Browse a paginated fashion catalogue
- Search products by name or type
- Filter products by category, size, and price
- Sort products by price, size, or newest arrivals
- View detailed product information, available sizes, stock status, and customer reviews
- Register, log in, update profiles, and change passwords
- Add products to a shopping cart
- Place and track orders
- Submit product reviews as an authenticated user

### Admin Features

- Manage products and categories
- Manage inventory and stock
- View and manage customer orders
- Access Django's secure admin panel

---

## 🛠️ Tech Stack

### Backend

- Python 3.12
- Django

### Database

- SQLite

### Frontend

- HTML
- CSS
- JavaScript
- Django Templates

### Third-Party Packages

- django-filter
- django-extensions
- django-widget-tweaks

---

## 🎥 Demo

https://github.com/user-attachments/assets/0e7a005e-2b41-409d-a788-dbb8f064adf4

---

## 📂 Project Structure

```text
velora-ecommerce/
│
├── ecommerce_site/      # Project configuration, shared templates & static assets
├── dashboard/           # Admin dashboard for products and categories
├── orders/              # Shopping cart, checkout, and order management
├── products/            # Products, categories, filters, and catalogue importer
├── users/               # Authentication, profiles, and shipping addresses
│
├── manage.py
├── requirements.txt
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.12+
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/ZahraYasin2209/velora-ecommerce.git
cd velora-ecommerce
```

### 2. Create a Virtual Environment (Recommended)

#### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

#### macOS/Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Apply Database Migrations

```bash
python manage.py migrate
```

### 5. Import the Sample Product Catalogue

```bash
python manage.py load_product_catalog_json_and_populate_models
```

### 6. Create an Administrator Account

```bash
python manage.py createsuperuser
```

### 7. Start the Development Server

```bash
python manage.py runserver
```

Open your browser and visit:

```
http://127.0.0.1:8000/
```

---

## 👤 Admin Panel

After creating a superuser, access the Django Admin Panel at:

```
http://127.0.0.1:8000/admin/
```

---

## 📌 Useful Commands

```bash
# Start development server
python manage.py runserver

# Check project configuration
python manage.py check

# Create migrations
python manage.py makemigrations

# Apply migrations
python manage.py migrate

# Create superuser
python manage.py createsuperuser

# Import sample product catalogue
python manage.py load_product_catalog_json_and_populate_models
```

---

## 🔮 Future Improvements

- Integrate online payment gateways (Stripe/PayPal)
- Wishlist functionality
- Product recommendation system
- Email notifications
- Real-time order tracking
- REST API using Django REST Framework
- Docker support
- PostgreSQL deployment
- Unit and integration testing
- CI/CD pipeline with GitHub Actions

---

## 📄 License

This project is intended for educational and portfolio purposes.

---

## 👩‍💻 Author

**Zahra Yasin**

Backend & GenAI Engineer

- GitHub: https://github.com/ZahraYasin2209
- LinkedIn: https://www.linkedin.com/in/zahra-yasin/
