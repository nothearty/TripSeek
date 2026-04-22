<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./frontend/src/assets/tripseekFont-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="./frontend/src/assets/tripseekFont-light.svg">
    <img alt="TripSeek Logo" src="./frontend/src/assets/tripseekFont-light.svg" width="300">
  </picture>
  <h1>🌍 TripSeek</h1>
  <p><strong>Your AI-Powered Personalized Travel Planner</strong></p>
  <p><i>Built for the <a href="https://ai.google.dev/competition/projects/tripseekai?hl=it">Google Gemini API Developer Competition</a></i></p>
</div>

## 📖 Overview

**TripSeek** is an intelligent travel planning application designed to create unique, personalized, and practical day-by-day itineraries. Say goodbye to generic travel guides—simply input your destination, the number of days, and your specific interests, and let our AI engine craft the perfect trip for you.

Created by **[@nothearty](https://github.com/nothearty)** and **[xenopers](https://github.com/xenopers)**.

## ✨ Features

- **🤖 AI-Powered Itineraries:** Utilizes Google's **Gemini 1.5 Flash** model to generate highly customized and realistic travel plans based on your hobbies and preferences.
- **🗺️ Interactive Maps:** Integrated interactive maps (powered by MapLibre and MapTiler) to visualize your daily routes, complete with numbered markers for each activity.
- **⚡ Fast & Modern Stack:** Built with Bun for blazing-fast performance on both the frontend and backend.
- **🔐 Secure Authentication:** Google OAuth integration with secure session management.

## 🛠️ Tech Stack

**Frontend:**
- [React](https://reactjs.org/) + [Vite](https://vitejs.dev/)
- [Tailwind CSS](https://tailwindcss.com/) & [Shadcn UI](https://ui.shadcn.com/) for styling
- [MapLibre GL JS](https://maplibre.org/) for interactive maps
- [TanStack Router](https://tanstack.com/router) & [React Query](https://tanstack.com/query)

**Backend:**
- [Bun](https://bun.sh/) runtime
- [Hono](https://hono.dev/) web framework
- [PostgreSQL](https://www.postgresql.org/) with [TypeORM](https://typeorm.io/)
- [Google Generative AI SDK](https://github.com/google/generative-ai-js)

---

## 🚀 Getting Started

This project uses [Bun](https://bun.sh/) for both the frontend and backend. Follow these instructions to set up and run the project locally.

### Prerequisites

Ensure you have Bun.js installed on your system.

**Windows:** Open PowerShell and run:
```sh
powershell -c "irm bun.sh/install.ps1 | iex"
```

**Linux/macOS:** Run in your terminal:
```sh
curl -fsSL https://bun.sh/install | bash
```

### 1. Backend Setup

Navigate to the backend directory and install dependencies:
```sh
cd backend
bun install
```

Create a `.env` file in the `backend` directory with the following structure:
```env
DB_PASSWORD=your_database_password
DB_NAME=your_database_name
DB_USER=your_database_user
GOOGLE_CLIENT_ID=your_google_client_id
SESSION_ENCRYPTION_KEY=your_32_character_long_session_encryption_key
GOOGLE_CLIENT_SECRET=your_google_client_secret
GEMINI_API_KEY=your_gemini_api_key
GOOGLE_PLACES_API_KEY=your_google_places_api_key
```

**Environment Variables Description:**
- `DB_PASSWORD`: The password for your PostgreSQL database.
- `DB_NAME`: The name of the database you're using.
- `DB_USER`: The database user name.
- `GOOGLE_CLIENT_ID`: The client ID for Google OAuth.
- `SESSION_ENCRYPTION_KEY`: A key used to encrypt session data (must be exactly 32 characters).
- `GOOGLE_CLIENT_SECRET`: The client secret for Google OAuth.
- `GEMINI_API_KEY`: API key for the Google Gemini API.
- `GOOGLE_PLACES_API_KEY`: API key for the Google Places API.

Start the backend server:
```sh
bun run dev
```

### 2. Frontend Setup

Open a new terminal, navigate to the frontend directory, and install dependencies:
```sh
cd frontend
bun install
```

Start the frontend development server:
```sh
bun run dev
```

### 3. Running the Application

After completing the setup, you should have two terminals running:
- **Backend Server:** `http://localhost:3000`
- **Frontend App:** `http://localhost:5173`

Visit `http://localhost:5173` in your browser to start planning your next trip!
