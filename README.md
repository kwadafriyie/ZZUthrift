# ZZU Thrift

A student-to-student marketplace built exclusively for Washington State University students. Buy. Sell. Save. Repeat.

ZZU Thrift helps WSU students resell clothes, textbooks, tech, and dorm essentials in a campus-focused marketplace, because paying full price is optional.

**Status:** Hackathon prototype built in 24 hours. Core features work, but the project is not production-ready.

## Team & My Role

Built by a team of 4 at the 24-hour **CrimsonCode Hackathon** (February 2026): [@chanceshungu](https://github.com/chanceshungu), [@mohassan9989](https://github.com/mohassan9989), [@funkycoder123](https://github.com/funkycoder123), and me.

I built the backend: the Express REST API and MongoDB data layer, passwordless Magic Link authentication with JWT sessions restricted to @wsu.edu emails, and the Docker Compose setup that gave the whole team an identical development environment. We presented the working app to the hackathon judges.

This repo is a mirror of our team's original private repository, with full commit history.

## Hackathon Theme: Reinventing the Wheel

Instead of building something unheard of, we asked: what if we took something that already works and made it better for one specific community?

We reinvented Depop. It's a strong resale platform, but it serves a global audience, with no campus verification, no focus on student budgets, and no community trust layer. ZZU Thrift keeps the resale idea and rebuilds it for WSU: student-only access, college-friendly pricing, local meetups, and WSU-inspired branding.

Depop connects strangers. ZZU Thrift connects classmates.

## Features

**Authentication**
- Passwordless Magic Link sign-in, restricted to @wsu.edu email addresses
- JWT-based sessions and protected routes

**Listings**
- Create, edit, and delete listings with images, title, price, description, and category
- Item detail pages

**Search & Filtering**
- Keyword search, category filters, and price sorting

**Messaging**
- Direct buyer-to-seller conversations with an inbox

**Favorites & Profiles**
- Save items and view them from your profile
- Manage your active listings and edit profile info

## Tech Stack

- **Frontend:** React, Zustand (state management), Tailwind CSS
- **Backend:** Node.js, Express, REST API, JWT
- **Database:** MongoDB
- **Dev Environment:** Docker Compose

## Project Structure

```
ZZUthrift/
├── backend/             # Express REST API, auth, MongoDB models
├── frontend/            # React + Zustand + Tailwind client
├── docker-compose.yml   # Runs frontend, backend, and database together
└── README.md
```

## Installation & Setup

**Prerequisites:** Git and Docker Desktop

1. Clone the repository:
```bash
git clone https://github.com/kwadafriyie/ZZUthrift.git
cd ZZUthrift
```

2. Create `backend/.env` with:
```
JWT_SECRET=your-own-long-random-string
OPENAI_API_KEY=your-key-here   # optional
```
`MONGO_URI` defaults to the Docker database, so you only need to set it to use a different MongoDB instance.

3. Build and start everything:
```bash
docker compose up --build
```

4. Open the app at `http://localhost:3000` (the API runs on `http://localhost:8000`)

## Future Improvements

- Admin dashboard and moderation/reporting
- User rating system
- Push notifications
- Mobile app version
