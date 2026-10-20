# Task Manager API

Express and MongoDB API for Task Manager.

Run `npm install`, copy `.env.example` to `.env`, set a strong random `JWT_SECRET`, start MongoDB, then run `npm start`. API listens on port 3000.

Authentication: `POST /auth/register`, `POST /auth/login`, `GET /auth/me`. Authenticated task routes: `GET/POST /tasks`, `GET/PUT/DELETE /tasks/:id`, and `GET /tasks/debug/cache`.

NodeCache caches responses for 60 seconds, uses per-user keys, and invalidates affected task cache entries on writes. Cache is process-local and clears on restart.
