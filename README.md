# FoodZone 🍕🍔

A PHP & MySQL web application for food ordering and delivery management. Features client ordering, delivery courier tracking, and an administrative dashboard with automated email notifications via Mailjet.

---

## 🚀 Features

- **Client Portal**: Browse food items, place orders, and manage profile.
- **Admin Dashboard**: Manage users, monitor orders, and oversee restaurant activity.
- **Delivery Management (Livreur)**: View assigned deliveries and update order status (`EN_ATTENTE`, `EN_COURS`, `LIVREE`, `ANNULEE`).
- **Email Notifications**: Automated email notifications to customers upon delivery status updates using Mailjet API.
- **Authentication**: Secure registration and login with bcrypt password hashing and session management.

---

## 🛠️ Tech Stack

- **Backend**: PHP 8+
- **Database**: MySQL / MariaDB
- **Architecture**: MVC (Model-View-Controller)
- **Dependencies**: Composer, [Mailjet PHP SDK](https://github.com/mailjet/mailjet-apiv3-php)
- **Frontend**: HTML5, CSS3, JavaScript, jQuery, Bootstrap

---

## 📁 Project Structure

```text
FoodZone-taher/
├── app/
│   ├── controllers/      # Application controllers
│   ├── models/           # Data models and business logic
│   └── views/            # UI templates (admin, client, livreur, auth)
├── config/
│   └── Database.php      # PDO database connection
├── public/
│   ├── admin-assets/     # Admin panel styles, scripts, fonts
│   ├── client-assets/    # Client storefront assets
│   ├── login_register-assets/
│   └── *.php             # Entry points
├── foodzone.sql          # Database schema and seed data
├── composer.json         # PHP dependencies
├── .env.example          # Environment variable template
└── README.md
```

---

## ⚙️ Setup & Installation

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/FoodZone-taher.git
cd FoodZone-taher
```

### 2. Install dependencies
Ensure you have [Composer](https://getcomposer.org/) installed:
```bash
composer install
```

### 3. Setup the database
1. Start your MySQL server (via XAMPP, WampServer, Docker, or native MySQL).
2. Create a database named `foodzone`.
3. Import `foodzone.sql`:
   ```bash
   mysql -u root -p foodzone < foodzone.sql
   ```
   *(Or import via phpMyAdmin)*

### 4. Configure environment variables
Copy `.env.example` to `.env`:
```bash
cp .env.example .env
```
Update `.env` with your database credentials and Mailjet API keys:
```env
MAILJET_API_KEY=your_mailjet_public_key
MAILJET_SECRET_KEY=your_mailjet_private_key
MAILJET_SENDER_EMAIL=your_email@example.com

DB_HOST=localhost
DB_NAME=foodzone
DB_USER=root
DB_PASS=
```

### 5. Run the application
Using Apache (e.g. XAMPP/WAMP):
Place the project in your `htdocs` or `www` directory and navigate to:
```
http://localhost/FoodZone-taher/public/
```

Or using PHP's built-in server from the `public` directory:
```bash
cd public
php -S localhost:8000
```
Then visit `http://localhost:8000`.

---

## 📄 License
This project is open-source under the [MIT License](LICENSE).
