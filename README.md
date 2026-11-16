# Personal Profile App

A small Express.js server that serves a personal profile through a few text routes and a JSON API endpoint.

> This is a practice project built as part of the **freeCodeCamp Back End Development and APIs** certification ("Build a Personal Profile App").

## Purpose

The app demonstrates the basics of building a web server with Node.js and Express: creating an app, defining `GET` routes, sending plain-text responses, and returning structured JSON from an API endpoint.

## Express.js Implementation

- `server.js` creates an Express application with `express()`.
- Each route is registered with `app.get(path, handler)`.
- Text routes respond with `res.send(...)`.
- The API route responds with `res.json(...)`, which sets the `Content-Type: application/json` header automatically.
- The server listens on port **3000** via `app.listen(PORT, ...)`.

## Available Routes

| Method | Route | Response type | Response |
|---|---|---|---|
| GET | `/` | Text | `Welcome to Camper Bot's homepage!` |
| GET | `/hobbies` | Text | `I cycle, go boating, and play guitar.` |
| GET | `/skills` | Text | `JavaScript, Node.js, and Express.js!` |
| GET | `/api/profile` | JSON | Profile object (see below) |

## JSON API Response

`GET /api/profile` returns:

```json
{
  "name": "Camper Bot",
  "hobbies": ["cycling", "boating", "guitar"],
  "skills": ["JavaScript", "Node.js", "Express.js"]
}
```

## Installation

Requires [Node.js](https://nodejs.org/) 18 or later.

```bash
git clone https://github.com/FedaaM7md/fcc-personal-profile-app.git
cd fcc-personal-profile-app
npm install
```

## Running the App

```bash
node server.js
```

The server starts on `http://localhost:3000`. Try it:

```bash
curl http://localhost:3000/
curl http://localhost:3000/api/profile
```

## Technologies

- Node.js
- Express.js 5

## Project Structure

| File | Purpose |
|---|---|
| `server.js` | Express server and route definitions |
| `package.json` | Project metadata and the Express dependency |
| `package-lock.json` | Locked dependency versions for reproducible installs |

## Attribution

Built for the [freeCodeCamp](https://www.freecodecamp.org/) Back End Development and APIs curriculum.

## Author

Fedaa Mohamed ([@FedaaM7md](https://github.com/FedaaM7md))
