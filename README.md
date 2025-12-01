# SC2006 - SmartCommute

- A website that helps commuters find MRT/LRT stations, plan routes and receive alerts. This repository contains front-end code in the 'SmartCommute_FrontEnd' folder, and back-end code in the 'SmartCommute_BackEnd' folder

- Demo Video: https://youtu.be/y6PVm2eFhJ0

---

## Repository layout

- `SmartCommute_FrontEnd/` — frontend (Vite + React)
  - `package.json` — frontend scripts and dependencies
  - `src/` — React app, components, API helpers and static data
  - `public/` — static assets

- `SmartCommute_BackEnd/` — backend (Node.js + Express + MongoDB)
  - `app.js` — application entrypoint
  - `src/` — controllers, models, routes, middleware, and static backend data
 

---

## Quick summary

- Frontend: React app using Vite. Main entry: `src/main.jsx`.
- Backend: Express API with JWT auth and MongoDB (Mongoose). Controllers live in `SSmartCommute_BackEnd/src/controllers`.


---

## Prerequisites

- Node.js (recommended v18+)
- npm (comes with Node.js)
- For backend development: MongoDB (local or Atlas)

---

## Frontend — run locally

1. Open a terminal in `SmartCommute_FrontEnd/` (root of the frontend folder).
2. Install dependencies:

```powershell
npm install
```

3. Start the dev server:

```powershell
npm run dev
```


Useful frontend scripts (see `SmartCommute_FrontEnd/package.json`):

- `dev` — start Vite dev server
- `build` — produce production build
- `preview` — preview the production build
- `lint` — run ESLint
- `devStart` — legacy script (nodemon server.js) if using an express server for static hosting

---

## Backend — pointer to full instructions

The backend lives in `SmartCommute_BackEnd/`. It already includes a dedicated setup guide and database documentation. Please follow those for backend setup instead of duplicating steps here.



Quick start (short):

```powershell
cd SC2006-SmartCommute-backend

npm install

# create a .env file (see BACKEND_SETUP.md for required keys)

npm start
```

By default the backend uses `nodemon app.js` per `SmartCommute_BackEnd/package.json` and starts the API (the guide in `BACKEND_SETUP.md` has environment variable examples like `MONGODB_URI`, `JWT_SECRET`, and `LTA_ACCOUNT_KEY`).

---

## Development notes

- Frontend API helpers call backend endpoints under `/api/*` (see `src/api/` in the frontend folder).
- Backend controllers are organized under `SmartCommute_FrontEnd/src/controllers` and routes under `SmartCommute_FrontEnd/src/routes`.
- Static sample data is included in both projects under `data/`.

---

## Contributing

If you'd like to contribute:

1. Fork the repository and open a branch for your feature/bugfix.
2. Open a pull request describing the change.

