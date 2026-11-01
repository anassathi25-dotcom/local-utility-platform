# HandyHub — Local Utility & Maintenance Helper Locator

A full-stack starter for connecting customers with nearby service professionals.

## Features
- Responsive React + Vite customer website
- Browse/search providers by service, area, and keyword
- Provider profiles, pricing, experience, ratings, and availability
- JWT registration/login with bcrypt password hashing
- Create and track service bookings
- Provider dashboard endpoints and booking status updates
- Reviews with rating validation
- MongoDB/Mongoose models, input validation, Helmet, CORS, rate limiting
- Demo seed data and environment-based configuration

## Requirements
- Node.js 20+
- MongoDB 6+ (local or MongoDB Atlas)

## Run locally
1. Copy `server/.env.example` to `server/.env` and set `MONGODB_URI` and `JWT_SECRET`.
2. From the project root run:
   ```bash
   npm install
   npm run seed
   npm run dev
   ```
3. Open the Vite URL shown in the terminal (normally http://localhost:5173).

Demo login after seeding:
- Customer: `customer@demo.com` / `DemoPass123!`
- Provider: `electrician@demo.com` / `DemoPass123!`

## Production checklist
- Set strong unique `JWT_SECRET`, `CLIENT_ORIGIN`, and managed MongoDB credentials.
- Serve behind HTTPS; configure a production CORS origin.
- Add email/SMS verification and password reset before public launch.
- Add payment provider integration only after defining cancellation/refund policy.
- Configure database backups, monitoring, structured logs, and error alerting.
- Add object storage for provider photos/documents; validate and scan uploads.
- Review local privacy, consumer protection, tax, and worker-verification requirements.
- Run `npm audit`, tests, and load/security testing before deployment.

This is a deployable application foundation, not a claim of independently audited production readiness. Authentication and booking flows work; external SMS, payments, identity verification, and map/geocoding require provider credentials and product decisions.
