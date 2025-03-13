# Secrets
## Overview
This is a educational project built using NodeJS, Express and PostgreSQL. It supports authentication via OAuth (using Passport.js) and local authentication with password encryption (bcrypt.js).

## Features
- User authentication with OAuth (Google) using Passport.js
- Local authentication with secure password hashing via bcrypt.js
- RESTful API with Express.js
- PostgreSQL as the database

## Running Locally
1. Clone the Repository
```bash
git clone https://github.com/Avirat2211/Secrets.git
cd Secrets/
```
2. Install dependencies
```bash
npm install
```
3. Set up environment variables
```env
GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=
SESSION_SECRET=
PG_USER=
PG_HOST=
PG_DATABASE=
PG_PASSWORD=
PG_PORT=
```
4. Set up the database
```sql
CREATE TABLE users (
    id SERIAL PRIMARY KEY UNIQUE,
    email VARCHAR(1000) UNIQUE NOT NULL,
    password VARCHAR(1000),
    secret TEXT
);
```
5. Start the server
```bash
node ./index.js
```
