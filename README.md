# 🖤 Black Phanter

![PHP](https://img.shields.io/badge/PHP-8.x-777BB4?logo=php)
![MySQL](https://img.shields.io/badge/MySQL-InnoDB-4479A1?logo=mysql)
![Apache](https://img.shields.io/badge/Server-Apache-D22128?logo=apache)
![Status](https://img.shields.io/badge/Status-Active-success)
![License](https://img.shields.io/badge/License-Proprietary-red)

> Eine modulare All-in-One Web-Plattform für **E-Commerce, Community & Content-Management** – entwickelt mit Fokus auf Performance, Sicherheit und Premium-Design.

---

## 📌 Übersicht

**Black Phanter** ist eine integrierte Web-Plattform, die folgende Systeme in einer einzigen Anwendung vereint:

- 🛒 Vollständiger Online-Shop
- 👥 Community-Forum & Social Features
- 📰 News / Blog System
- 🎫 Support-Ticket-System
- 🔐 Rollenbasiertes Admin-Panel

Das System wurde mit einem „Dark Premium“-UI-Ansatz und maximaler Performance entwickelt.

---

# 🚀 Features

## 🛒 E-Commerce

- Produktkatalog mit Filter & Sortierung
- AJAX-Warenkorb (Session-basiert)
- Mehrstufiger Checkout
- Gutschein-System
- Bewertungs-System (verifizierte Käufer)
- Bestellverwaltung & Status-Workflow
- PDF-Rechnungsgenerierung
- Lagerbestandsverwaltung

---

## 👥 Community

- Forum (Kategorien → Foren → Themen → Beiträge)
- Live-Aktivitätsfeed
- Leaderboard (EXP-System)
- Globaler Chat / PNs
- Beitrags-Meldesystem

---

## 📰 Content & Support

- News / Blog mit Kommentaren
- Globale Suche (Shop + Forum)
- Support-Ticket-System
- Admin-Moderation

---

# 🏗️ Technologie-Stack

| Bereich | Technologie |
|----------|-------------|
| Backend | PHP 8.x |
| Datenbank | MySQL / MariaDB (InnoDB) |
| Frontend | HTML5, CSS3, Vanilla JS (ES6+) |
| Server | Apache (XAMPP empfohlen) |
| Architektur | Modular, OOP + performanter prozeduraler Mix |

---

# 📂 Projektstruktur

```
/admin          → Admin-Panel
/api            → JSON & AJAX Endpoints
/assets         → Statische Ressourcen
/css            → Stylesheets
/js             → Frontend Logik
/includes       → Konfiguration & Helper
/maintenance    → DB-Tools & Fixes
/uploads        → Benutzer-Uploads
```

---

# ⚙️ Installation

## 1️⃣ Voraussetzungen

- PHP ≥ 8.0
- MySQL / MariaDB
- Apache (empfohlen: XAMPP)
- mod_rewrite aktiviert

---

## 2️⃣ Repository klonen

```bash
git clone https://github.com/TGH-Scripts/black-phanter.git
cd black-phanter
```

---

## 3️⃣ Datenbank einrichten

1. Neue Datenbank erstellen
2. SQL-Dump importieren
3. Konfiguration anpassen:

```php
// /includes/config.php

define('DB_HOST', 'localhost');
define('DB_USER', 'root');
define('DB_PASS', '');
define('DB_NAME', 'black_phanter');
```

---

## 4️⃣ Upload-Rechte setzen

```bash
chmod -R 755 uploads/
```

---

# 👤 Rollen & Rechte

| Rolle | Rechte |
|--------|--------|
| `user` | Shop, Forum, Tickets |
| `moderator` | Moderation, Admin-Zugang (eingeschränkt) |
| `admin` | Vollzugriff |

---

# 🔄 Bestellprozess

1. Produkt → Warenkorb (`$_SESSION['cart']`)
2. Checkout (Adresse → Versand → Zahlung)
3. Bestellung wird gespeichert (`shop_orders`)
4. Positionen werden übertragen (`shop_order_items`)
5. Lagerbestand wird reduziert
6. Bestätigungsmail wird versendet
7. Rechnung generierbar (`invoice.php`)

---

# 🔐 Sicherheitsmaßnahmen

- Prepared Statements (`mysqli_prepare`)
- Passwort-Hashing (`password_hash()` – BCRYPT)
- CSRF-Tokens
- Session-Regeneration
- XSS-Schutz (`htmlspecialchars()`)
- Optional 2FA
- Audit-Logs im Admin-Panel

---

# 🗄️ Zentrale Datenbanktabellen

- `site_users`
- `shop_products`
- `shop_orders`
- `shop_order_items`
- `shop_reviews`
- `forum_topics`
- `forum_posts`
- `support_tickets`

---

# 🛠️ Admin-Panel

Erreichbar unter:

```
/admin
```

Enthält:

- Dashboard
- Produktverwaltung
- Bestellverwaltung
- Gutschein-Management
- Benutzerverwaltung
- Support-Tickets
- Backups
- Audit-Logs

---

# 🎨 Design

- Dark Premium UI
- Accent Color: `#9b59b6`
- Glassmorphism
- Responsive Layout
- Mobile optimiert

---

# 📊 Roadmap

- Stripe Integration
- REST API Ausbau
- WebSocket Chat
- PWA Support
- Docker Setup

---

# 📝 Lizenz

Dieses Projekt ist proprietär.  
Nutzung nur mit ausdrücklicher Genehmigung.

---

# 👨‍💻 Autor

Erstellt: 14.02.2026  
Projekt: **Black Phanter Web-Plattform**

Development: **TGH-Scripts**
