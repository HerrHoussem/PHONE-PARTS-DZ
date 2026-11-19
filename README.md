# DZParts Algeria

A responsive, bilingual French/Arabic storefront prototype for original smartphone spare parts in Algeria. It is deployable on GitHub Pages without a build step.

## Included
- Brand/model/problem smart finder
- Search and category filters
- Technical product pages and grading
- Serialized SKU/test data
- Persistent cart using localStorage
- Algeria-oriented checkout form, COD, BaridiMob/CCP, Edahabia/CIB placeholders
- WhatsApp product inquiry
- Order reference and tracking demo
- PRO repair-shop application
- Admin KPI, order pipeline, low-stock and margin calculator
- Responsive mobile layout and RTL Arabic mode

## Run locally
Open `index.html`, or run:

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080`.

## Publish to GitHub Pages
1. Create a new public GitHub repository.
2. Upload all files from this project at the repository root.
3. Open **Settings > Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch `main` and folder `/ (root)`, then save.

## Production checklist
This is a functional front-end MVP, not a production commerce backend. Before launch:
- Replace demo products, phone number and images.
- Add authentication and server-side authorization.
- Connect PostgreSQL/Prisma or another secured backend.
- Integrate a confirmed Algerian payment provider for CIB/Edahabia.
- Integrate a delivery API and all 58 wilayas/communes.
- Store orders and inventory on the server, not localStorage.
- Add server-side validation, CSRF protection, rate limits, audit logs and backups.
- Configure legal identity, terms, privacy, warranty, returns, invoicing and customer-data handling for Algeria.
- Never publish full IMEI/serial numbers publicly; mask them and restrict access.

## Files
- `index.html`: pages/sections and forms
- `styles.css`: responsive UI and RTL layout
- `app.js`: inventory, filtering, cart, checkout, translations, admin demo
- `.github/workflows/pages.yml`: automatic GitHub Pages deployment
