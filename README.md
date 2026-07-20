# Velora

**Velora** is a full-stack Django e-commerce application for a fashion catalogue. It provides product discovery, filtering, account management, carts, checkout, product reviews, and a protected management dashboard.

## Highlights

- Browse a paginated product catalogue with search, category, size, price, and sort filters.
- View product details, available sizes, stock, descriptions, images, and customer reviews.
- Register, sign in, update a profile, and change a password.
- Add products to a cart and complete a checkout and order-review flow.
- Submit product reviews as an authenticated user.
- Manage products and categories through a role-protected dashboard.
- Import the sample catalogue from JSON with a custom Django management command.

## Built with

| Area | Technology |
| --- | --- |
| Backend | Python, Django |
| Database | SQLite (development) |
| Filtering | django-filter |
| Template utilities | django-widget-tweaks |
| Admin utilities | django-extensions |
| Frontend | Django templates, CSS, JavaScript |

## Getting started

### Prerequisites

- Python 3.12 or later
- Git

### Installation

```powershell
git clone https://github.com/<your-github-username>/velora-django-ecommerce.git
cd velora-django-ecommerce
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
python manage.py migrate
```

### Load the catalogue and run the app

The dataset is intentionally imported separately; starting the development server does not load it automatically.

```powershell
python manage.py load_product_catalog_json_and_populate_models
python manage.py runserver
```

Open [http://127.0.0.1:8000/](http://127.0.0.1:8000/) in a browser. The catalogue is at [http://127.0.0.1:8000/products/](http://127.0.0.1:8000/products/).

### Create an administrator

```powershell
python manage.py createsuperuser
```

The Django admin is available at [http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/). The app dashboard is available at `/admin_dashboard/` for users with the required role.

## Image-data note

The included JSON stores image URLs from an external third-party website. Those URLs can expire or reject requests from another site, which produces broken image icons even though the product records import correctly. For a production-ready project, use images you own or are licensed to use, save them locally under `media/` or upload them to your own cloud storage, and store those URLs in the database.

## Project structure

```text
ecommerce_site/       Project settings, root URLs, shared templates, and static files
products/              Catalogue models, filters, templates, and JSON import command
orders/                Cart, checkout, orders, and payments
users/                 Authentication, profiles, and shipping addresses
dashboard/             Role-protected product and category management UI
```

## Useful commands

```powershell
# Validate Django configuration
python manage.py check

# Create and apply new migrations after changing models
python manage.py makemigrations
python manage.py migrate

# Re-import the sample catalogue
python manage.py load_product_catalog_json_and_populate_models
```

## Repository hygiene

Do not commit `.venv/`, `venv/`, `db.sqlite3`, `.env`, or user-uploaded `media/` files. Keep migration files and `products/management/data/clothes.json` so a fresh clone can rebuild the database and load the catalogue.

Before deployment, move `SECRET_KEY`, `DEBUG`, database credentials, and `ALLOWED_HOSTS` into environment-based production settings.

## License

This project currently has no license. Add a license file before permitting reuse or contributions.
