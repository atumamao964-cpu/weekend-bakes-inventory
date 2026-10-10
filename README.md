# Weekend Bakes — Inventory (React + localStorage)

Pure **local-storage** inventory management for Weekend Bakes.  
No PHP, no MySQL, no backend — open the HTML file and it works.

## How to use

1. Open `index.html` in a modern browser (Chrome, Firefox, Edge, Safari).
2. Or serve it with any static server:
   ```bash
   npx serve .
   # or
   python -m http.server 8080
   ```

## Features

| Feature | Description |
|---------|-------------|
| **Stock controls** | + / − buttons and direct quantity edit |
| **Status badges** | In Stock · Low Stock (≤5) · Out of Stock |
| **Weekly reset** | Restore current stock → weekly stock for all products |
| **CRUD** | Add, edit, delete products |
| **Search & filters** | By name, category, status |
| **Alerts** | Low / out-of-stock banners |
| **Stats** | Products, total units, est. cost value |
| **History** | Last 200 stock change events |
| **Export / Import** | JSON backup of all inventory |
| **Reset data** | Clear localStorage and reseed original products |

## Data storage

Everything lives in the browser:

- `localStorage.wb_inventory_products` — product list + stock
- `localStorage.wb_inventory_history` — change log

Seed data matches the original Weekend Bakes product catalog (Cookies, Scoopable Cookies, Chewy Cookies, Banana Loaves).

## Tech

- React 18 (CDN)
- Babel standalone (for JSX in the browser)
- No build step required
