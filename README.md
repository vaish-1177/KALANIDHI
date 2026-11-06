# Kala-Nidhi

Kala-Nidhi is a full-stack artisan marketplace website for empowering local craftspeople and connecting them with buyers across India. The platform helps artisans showcase handcrafted products, manage listings, and reach customers while giving buyers a simple way to browse, search, and purchase authentic handmade goods.

## Overview

This project brings together:

- Artisan profiles with personal stories and craft specialties
- Buyer and artisan authentication flows
- Product listings with image uploads and camera capture
- Search, filtering, and voice-assisted discovery
- Wishlist, cart, and order tracking
- Multilingual access for Indian-language users
- Supabase-powered data storage and authentication

## Features

### For Artisans
- Create a seller profile
- Publish handmade products with price, category, description, and multiple images
- Edit or remove product listings
- Add personal craft story and location details
- Upload images or capture product photos from the camera

### For Buyers
- Browse products by category and search term
- View artisan profiles and product details
- Save products to wishlist and manage cart
- Review order status and shopping activity
- Explore a marketplace designed for handcrafted goods

### Platform Experience
- Responsive storefront and dashboard layout
- AI-style auto-generated product descriptions
- Voice-enabled search and dictation
- Multi-language support with English/Hindi and other Indian language options
- Supabase integration for auth, storage, and relational data

## Tech Stack

- Frontend: HTML, CSS, JavaScript
- Backend/Data: Supabase
- Edge Function: Deno (for price normalization check)
- Storage: Supabase storage and database tables
- Assets: Local image files and browser camera capture

## Project Structure

```text
Kala-Nidhi--main/
├── README.md
├── index.html
├── indexhindi.html
├── style.css
├── script.js
├── login.html
├── login.js
├── signup.html
├── buyer.html
├── buyer-signup.html
├── artisan_store.html
├── artisandashboard.html
├── assets/
├── supabase-schema.sql
├── supabase/
│   ├── config.toml
│   └── functions/
│       └── check-product-price/
│           ├── deno.json
│           └── index.js
└── package.json
```

## Prerequisites

- A modern browser
- Node.js and npm (recommended for local tooling and Supabase CLI)
- A Supabase project

## Setup

1. Clone the repository:

```bash
git clone <repository-url>
cd Kala-Nidhi--main
```

2. Install dependencies:

```bash
npm install
```

3. Configure Supabase:
   - Create a Supabase project in the Supabase dashboard
   - Update the Supabase URL and anon key in `script.js`
   - Apply the schema from `supabase-schema.sql`

4. Start the app locally:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Supabase Setup

The project includes a schema file for the database:

- `supabase-schema.sql` — creates profiles, products, wishlists, cart items, orders, and policies

For local Supabase development, you can also use the configuration under `supabase/`:

```bash
npx supabase start
```

## Notes

- The website is primarily a static frontend with client-side JavaScript and Supabase as the backend service.
- The project contains browser camera integration for image capture in registration and listing flows.
- Some language translations use Google Translate / MyMemory-like translation logic and route handling for Hindi and other regional language views.
- The edge function under `supabase/functions/check-product-price` normalizes and validates product pricing data.

## License

This project is distributed for educational and prototype/demo use unless a separate license is provided by the project owner.

## Future Improvements

- Add secure admin moderation tools
- Introduce payment integration for checkout
- Improve product reviews and seller analytics
- Expand product recommendations and AI-assisted discovery
- Deploy production-ready backend and storage configuration
