# API project with Docker Arcjet

An API project developed using Docker, Warp, Arcjet, with automated CI/CD, and a backend implemented with Node.js, Express.js, Neon Postgres, Drizzle ORM, and Zod—secure, scalable, and production-ready.

## Setup

1. Install eslint and prettier dependencies to format the code

```bash
npm i eslint  @eslint/js prettier eslint-config-prettier eslint-plugin-prettier -D
```

- After installing, you usually create an config file: `eslint.config.js` and `.prettierrc`
- Add the following scripts to `package.json` to format and lint the code

```json
    "lint": "eslint .",
    "lint:fix": "eslint . --fix",
    "format": "prettier --write .",
    "format:check": "prettier --check ."
```

2. Setup database using [NEON](https://neon.com/docs/guides/drizzle)
   - After Create db schema `models/user.model.js`, run `npm run db:generate`
   - Apply migrations to your Neon database `npm run db:migrate`

## Project Structure

The project is structured as follows:

1. `src`: Contains the source code for the API project.
   - `app.js`: all about setup the server (express) with the routes and middleware
   - `server.js`: runs the server
   - `index.js`: Starting point of the application
   - middleware: contains all the middleware functions
   - models: database schema
   - routes: contains all the api routes
