# Auth Foundation (Secure Authentication System)

A custom built authentication foundation designed for real-world web applications and SaaS products.

This project implements a secure, scalable authentication flow from scratch using modern technologies, no third-party auth services.

---

Features

Authentication
- Secure signup and login
- Argon2 password hashing
- Server-side session management with cookies
- Hashed session tokens (SHA-256 digest)
- `/api/auth/me` endpoint to fetch current user
- Route protection with server middleware
- Logout that revokes server session
Security
- httpOnly secure cookies
- Session expiry
- Protection against session reuse
- Middleware guard for protected pages
- (Future) CSRF protection
- (Future) Rate limiting


Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | Next.js (App Router) |
| Backend | Next.js API Routes |
| Authentication | Argon2, Cookie Sessions |
| Database | PostgreSQL |
| ORM | Prisma |
| Environment | Docker, Docker Compose |
| Deployment | Recommend Vercel / Railway |



Getting Started

Requirements
- Node.js 18+
- Docker & Docker Compose

Setup

```bash
git clone https://github.com/Jengazar/auth-foundation.git
cd auth-foundation
cp .env.example .env
# update .env DATABASE_URL
docker compose up -d
npm install
npx prisma migrate dev
npm run dev
