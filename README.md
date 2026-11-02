# Zaheer Seed Corporation — Frontend

The official customer-facing website for **Zaheer Seed Corporation** (crop seed breeding, processing, and distribution from Kasur, Pakistan).

---

## Overview

This repository contains the complete frontend client for the Zaheer Seed Corporation website:
- **Interactive Seed Catalogue**: Filter seeds by crop category (Wheat, Rice, Maize, Cotton, etc.) loaded dynamically from the backend API.
- **Cart & Order System**: Add seeds to cart, adjust quantities, and submit order requests.
- **Inquiry & Contact Form**: Directly sends customer inquiries to the backend database with instant WhatsApp fallback.
- **High-Performance**: Pure semantic HTML, responsive CSS, lightweight SVG vector illustrations, and vanilla JavaScript without heavy framework overhead.

---

## Getting Started

### Run Locally
You can run the frontend with any static web server:

**Using Python:**
```bash
python -m http.server 8000
```

**Using Node.js (`serve`):**
```bash
npx serve .
```

**Using VS Code:**
Install the "Live Server" extension and click **Go Live**.

Open `http://localhost:8000` (or `http://localhost:3000`) in your browser.

---

## Connecting with the Backend (`zsbackend`)

The frontend interacts with the REST API provided by [zsbackend](https://github.com/syednehajafferyy/zsbackend.git):
- `GET /api/categories` — Fetches active seed categories
- `GET /api/products` — Fetches published seed products
- `POST /api/inquiries` — Submits contact messages and cart order requests

### Configuring the Backend URL
If your backend is deployed on a different domain (e.g. `https://zsbackend.vercel.app`), configure the `API_BASE` in `index.html`:
```html
<script>
  window.API_BASE = "https://your-backend-url.vercel.app";
</script>
```
If hosted on the same domain or behind a reverse proxy, leave `API_BASE` empty to use relative paths (`/api/*`).

---

## Deployment

Deployable instantly to any static hosting provider:
- **GitHub Pages**: Go to repository Settings &rarr; Pages &rarr; Source: `Deploy from branch main /root`.
- **Vercel**: Import the repository and deploy with default static settings.
- **Netlify**: Drag and drop the folder or connect via GitHub.
