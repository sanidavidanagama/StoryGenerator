# Interactive Story Generator AI Frontend

A modern, interactive frontend for the **StoryGenerator** application, built with React and Vite. This project allows users to generate, play, and load stories based on custom themes.

---

## Table of Contents

- [Features](#features)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
    - [Running the App](#running-the-app)
- [Available Scripts](#available-scripts)
- [Configuration](#configuration)
- [Component Overview](#component-overview)
- [Development](#development)
- [References](#references)

---

## Features

- Generate stories based on user-provided themes.
- Play interactive story games.
- Load and display previously generated stories.
- Responsive and modern UI.
- Fast development with Vite and React.

---

## Project Structure

```
frontend/
│
├── .env                  # Environment variables
├── .gitignore            # Git ignore rules
├── eslint.config.js      # ESLint configuration
├── index.html            # Main HTML file
├── package.json          # Project metadata and dependencies
├── README.md             # Project documentation
├── vite.config.js        # Vite configuration
│
├── public/               # Static assets
│
└── src/                  # Source code
        ├── App.css
        ├── App.jsx           # Main App component
        ├── index.css
        ├── main.jsx          # Entry point
        ├── util.js           # Utility functions
        │
        └── components/
                ├── LoadingStatus.jsx
                ├── StoryGame.jsx
                ├── StoryGenerator.jsx
                ├── StoryLoader.jsx
                └── ThemeInput.jsx
```

---

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v16+ recommended)
- [npm](https://www.npmjs.com/) (comes with Node.js)

### Installation

1. **Clone the repository:**
     ```bash
     git clone https://github.com/sanidavidanagama/StoryGenerator.git
     cd frontend
     ```

2. **Install dependencies:**
     ```bash
     npm install
     ```

### Running the App

Start the development server:

```bash
npm run dev
```

The app will be available at [http://localhost:5173](http://localhost:5173) (default Vite port).

---

## Available Scripts

- `npm run dev` — Start the development server.
- `npm run build` — Build the app for production.
- `npm run preview` — Preview the production build.
- `npm run lint` — Run ESLint on the source code.

---

## Configuration

- **Environment Variables:**  
    Place any required variables in the `.env` file at the project root.
- **API Base URL:**  
    To run the frontend locally, set `API_BASE_URL` in `src/util.js` to `"/api"`.  
    Example:
    ```js
    export const API_BASE_URL = "/api"
    ```
    This ensures API requests are correctly routed during local development.
- **Vite Config:**  
    Modify `vite.config.js` for custom Vite settings.
- **ESLint:**  
    Linting rules are defined in `eslint.config.js`.

---

## Component Overview

- **App.jsx**  
    Main application component, sets up routing and layout.

- **components/ThemeInput.jsx**  
    Input for users to provide a theme for story generation.

- **components/StoryGenerator.jsx**  
    Handles story generation logic and UI.

- **components/StoryGame.jsx**  
    Interactive story game interface.

- **components/StoryLoader.jsx**  
    Loads and displays previously generated stories.

- **components/LoadingStatus.jsx**  
    Displays loading indicators and status messages.

- **util.js**  
    Utility functions used across components.

---

## Development

- **Styling:**  
    Uses CSS files (`App.css`, `index.css`) for styling.
- **React:**  
    Functional components with hooks.
- **Vite:**  
    Fast build and hot module replacement.


## References

- [React](https://react.dev/)
- [Vite](https://vitejs.dev/)
- [ESLint](https://eslint.org/)

> **Note:**  
> All creative work in this project is not my own. This repository is solely for tutorial purposes, based on the YouTube tutorial by [Tech With Tim](https://youtu.be/_1P0Uqk50Ps?si=BuDYSWagQn5lsix-).
