# Fullstack rest API in TypeScript and Go(Next 14, Go, Postgres, Docker)


## Overview

Welcome to our project! 🚀 This is a special blend of Go, PostgreSQL, and Next.js 14, working together to handle user-related actions. Buckle up for some CRUD magic!

## Getting Started

### Prerequisites
- Docker
- Docker Compose

### Quick Setup
1. Clone the project.
2. Go to the project folder.

### Let the Show Begin
Open your terminal and start the party:

```bash
docker-compose up -d db  # Start the database
docker-compose up        # Launch Go backend, PostgreSQL, and Next.js frontend
```
# VIP Access: Database Connection

Want to peek behind the scenes? Connect to the database:
```bash
docker exec -it db psql -U postgres
```

# Prepping Next.js to be containarized

In next.config.js, change:
```bash
const nextConfig = {
  reactStrictMode: true,
}
```
to:
```bash
const nextConfig = {
  output: 'standalone',
};
```
Finding Your Spot

    Frontend: http://localhost:3000
    Backend API: http://localhost:8000

Behind the Scenes: Environment Variables
For the Frontend (nextapp)

    NEXT_PUBLIC_API_URL: Go backend API URL (default: http://localhost:8000)

For the Go Backend (goapp)

    DATABASE_URL: PostgreSQL database connection URL

For the PostgreSQL Database (db)

    POSTGRES_USER: Username (default: postgres)
    POSTGRES_PASSWORD: Password (default: postgres)
    POSTGRES_DB: Database name (default: postgres)

Notes Backstage

    Ensure Docker and Docker Compose are installed.
    Check out Dockerfiles (next.dockerfile and go.dockerfile) for image secrets.
