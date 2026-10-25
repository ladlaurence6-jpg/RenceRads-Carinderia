# Rence/Rads Carinderia — Online Ordering System

A simple online ordering website for a Filipino carinderia in Davao City. Customers browse the menu, add dishes to a cart, and place orders. The owner manages the menu and orders from an admin dashboard.

**Live site:** https://ladlaurence6-jpg.github.io/

## Features

**For customers**
- Browse the menu by category (Main Dishes, Soups & Stews, Vegetables, Noodles, Rice & Drinks) and search by name
- Cart with quantity controls and a running total
- Checkout with Cash on Delivery or pickup
- Customer account with a personal dashboard that tracks only their own orders
- Change password

**For the owner (admin)**
- Dashboard with order and sales summary
- Manage Orders: update each order's status
- Menu CRUD: add, edit, delete dishes, and mark dishes sold out
- Download the menu as a file to publish it on the live website

## Project structure

```
index.html     The whole website (pages, styles, and logic)
menu-data.js   The published menu (generated from the admin page)
images/        Dish photos
README.md      This file
```

## Demo accounts

| Role | Email | Password |
|---|---|---|
| Admin | admin@rencerads.com | admin123 |
| Customer | client@rencerads.com | client123 |

These are demo logins built into the code. **Change them before real use** (edit `DEFAULT_USERS` in `index.html`), because anyone can read them in this public repository.

## Updating the menu on the live site

The admin page saves menu changes in the browser you are using, so they do not appear on the live site by themselves. To publish them:

1. Log in as admin and open **Menu CRUD**.
2. Make your changes (add dishes, edit prices, and so on).
3. Click **Download menu-data.js**.
4. Replace the `menu-data.js` file in this project with the downloaded one.
5. Put any new dish photos in the `images/` folder.
6. Commit and push to GitHub, then wait a minute or two and press Ctrl+F5 on the live site.

If a browser shows an old menu, use **Reset to Published Menu** on the Menu CRUD page.

## Run it on your computer

No install is needed. Open `index.html` in a browser, or use the Live Server extension in VS Code.

## Built with

- HTML, CSS, and JavaScript (no framework, no build step)
- [Tailwind CSS](https://tailwindcss.com/) via CDN
- [Font Awesome](https://fontawesome.com/) icons
- Inter font from Google Fonts
- Hosted on GitHub Pages

## Known limitations

This project has no server or database. Because of that:

- Accounts, orders, and the cart are stored in each visitor's own browser, so an order placed on one device is not visible on another, including to the owner.
- Passwords are stored as plain text in the browser, and login checks happen on the visitor's own device. This is fine for a demo or school project but not for real customer data.

To take real orders, the system needs a backend (for example Firebase or Supabase) to store accounts and orders securely.

## Contact

Rence/Rads Carinderia  
McArthur Highway, Matina, Davao City  
+63 917 123 4567
