# Dev Forum

Dev Forum is an online platform where software developers can showcase their portfolios, bid on projects, and connect with recruiters to get hired.

<img alt='screenshot' src='https://mir-s3-cdn-cf.behance.net/project_modules/fs_webp/508a45121098563.68c131f10f6fb.png' />

## Stack

- Next.js 14 (App Router)
- Shadcn/UI
- Tailwind CSS
- Prisma/Postgres
- Docker (for containerized setup)

---

# Setup & Installation

## Option 1: Recommended (Docker Setup)

> Prerequisite: Install Docker Desktop (Windows/Mac) or Docker Engine (Linux)

### Clone repository

```cmd
git clone https://github.com/saifulshihab/dev-forum.git
cd dev-forum
```

### Configure environment file

```cmd
cp .env.example .env
```

Edit `.env` and set required values.

### Run with Docker

```cmd
docker compose up --build
```

### Access Application

```text
http://localhost:3000
```

This method automatically starts:

- Dev Forum application
- PostgreSQL database

No need to manually install Node.js or PostgreSQL.

---

## Option 2: Manual Local Setup

### Clone the repository

```cmd
git clone https://github.com/saifulshihab/dev-forum.git
cd dev-forum
```

### Install dependencies

```cmd
npm install
```

### Environment variables

There is an `.env.example` file. Copy it to `.env`

```cmd
cp .env.example .env
```

Open `.env` and set all necessary values.

### Database setup with Prisma

Generate Prisma client:

```cmd
npx prisma generate
```

Run migrations:

```cmd
npx prisma migrate deploy
```

or for development:

```cmd
npx prisma migrate dev
```

### Build / Start application

Development mode:

```cmd
npm run dev
```

Production build:

```cmd
npm run build
npm start
```

---

## Live