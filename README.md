# Arogya Veda India

A full-stack Ayurvedic/herbal wellness storefront built with React + Vite on the client and Node.js + Express + MySQL on the server.

## Stack

- React 19 + Vite
- React Router
- Tailwind CSS
- Node.js + Express
- MySQL + mysql2
- JWT authentication
- bcryptjs
- Multer + Sharp for product photos

## Important

The backend is **CommonJS**. There is no MongoDB or Mongoose code in the server.

The public site layout is inspired by the information architecture of modern Ayurvedic ecommerce sites: announcement bar, catalogue navigation, hero, category discovery, bestseller products, new arrivals, educational content, newsletter and footer. Branding, logo and copy are Arogya Veda-specific.

## Setup


### 2. Configure server

```bash
cd server
cp .env.example .env
```

Set your MySQL credentials and a JWT secret of at least 32 characters.

### 3. Install server packages

```bash
npm install
```

### 4. Create tables and demo data

```bash
npm run seed
```

### 5. Start backend

```bash
npm run dev
```

Backend: `http://localhost:5000`

Health check: `http://localhost:5000/api/health`

### 6. Start frontend

```bash
cd ../client
npm install
npm run dev
```

Frontend: `http://localhost:5173`

## Admin

Set these values in `server/.env`:

```env
ADMIN_NAME=Arogya Veda Admin
ADMIN_EMAIL=admin@arogyaveda.local
ADMIN_PASSWORD=ChangeMe123!
```

Then:

```bash
npm run create:admin
```

Change the password before production use.

## Product photos

Admin product management supports JPEG, PNG, WEBP and AVIF uploads. Images are optimized to WebP and stored under:



## Production

Use HTTPS, a strong JWT secret, a non-root MySQL user, restricted database permissions, secure CORS origins, regular database backups and an external object-storage service for large product media if the catalogue grows.
