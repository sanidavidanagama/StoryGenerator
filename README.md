# Interactive Story Generator AI

**StoryGenerator** is a full-stack application that empowers users to generate, play, and manage AI-powered stories based on custom themes. The project is split into a robust Python FastAPI backend and a modern React + Vite frontend, designed for scalability, modularity, and ease of use.

---

## Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Features](#features)
- [Directory Structure](#directory-structure)
- [Getting Started](#getting-started)
    - [Backend Setup](#backend-setup)
    - [Frontend Setup](#frontend-setup)
- [Configuration](#configuration)
- [API Documentation](#api-documentation)
- [Development & Contribution](#development--contribution)
- [References](#references)
- [License](#license)

---

## Overview

StoryGenerator enables users to create unique stories using Large Language Models (LLMs), play interactive story games, and manage their story library. The backend handles story generation, job management, and data persistence, while the frontend provides an intuitive, responsive user interface.

---

## Architecture

- **Backend:**  
  Located in [`backend/`](./backend/), built with Python, FastAPI, SQLAlchemy, and Pydantic. Handles RESTful APIs, story generation, job management, and database operations.

- **Frontend:**  
  Located in [`frontend/`](./frontend/), built with React and Vite. Offers a modern, interactive UI for generating and playing stories.

- **Project Root:**  
  This file (`README.md`) and the [LICENSE](./LICENSE) file provide project-wide documentation and legal information.

---

## Features

- **AI-Powered Story Generation:**  
  Generate stories from custom prompts using LLMs (Google GenAI API).

- **Interactive Story Games:**  
  Play and interact with generated stories.

- **Job Management:**  
  Asynchronous job handling for story generation.

- **Story Library:**  
  Load and manage previously generated stories.

- **RESTful API:**  
  Well-structured endpoints for stories and jobs.

- **Modern Frontend:**  
  Responsive, fast, and user-friendly interface.

- **Environment-Based Configuration:**  
  Easily configurable for different environments.

---

## Directory Structure

```
StoryGenerator/
│
├── backend/         # FastAPI backend (see backend/README.md)
│   ├── core/
│   ├── db/
│   ├── models/
│   ├── routers/
│   ├── schemas/
│   ├── main.py
│   ├── requirements.txt
│   ├── pyproject.toml
│   ├── .env
│   └── README.md
│
├── frontend/        # React + Vite frontend (see frontend/README.md)
│   ├── public/
│   ├── src/
│   ├── package.json
│   ├── vite.config.js
│   ├── .env
│   └── README.md
│
├── README.md        # Project-wide documentation (this file)
└── LICENSE          # License file (to be created)
```

- For detailed backend and frontend documentation, see [`backend/README.md`](./backend/README.md) and [`frontend/README.md`](./frontend/README.md).

---

## Getting Started

### Backend Setup

1. **Navigate to the backend directory:**
    ```bash
    cd backend
    ```

2. **Install [uv](https://github.com/astral-sh/uv) for Python project management:**
    ```bash
    pip install uv
    ```

3. **Create and activate a virtual environment:**
    ```bash
    uv venv
    # On Unix/macOS:
    source .venv/bin/activate
    # On Windows:
    .venv\Scripts\activate
    ```

4. **Install dependencies:**
    ```bash
    uv sync
    ```

5. **Configure environment variables:**  
   Copy `.env.example` to `.env` and set your values (see [Configuration](#configuration) and [`backend/README.md`](./backend/README.md)).

6. **Run the FastAPI server:**
    ```bash
    uv run main.py
    ```

7. **API docs available at:**  
   [http://localhost:8000/docs](http://localhost:8000/docs)

---

### Frontend Setup

1. **Navigate to the frontend directory:**
    ```bash
    cd frontend
    ```

2. **Install dependencies:**
    ```bash
    npm install
    ```

3. **Configure environment variables:**  
   Copy `.env.example` to `.env` and set your values (see [`frontend/README.md`](./frontend/README.md)).

4. **Start the development server:**
    ```bash
    npm run dev
    ```

5. **App available at:**  
   [http://localhost:5173](http://localhost:5173)

---

## Configuration

- **Backend:**  
  Environment variables are managed via `.env` in `backend/`.  
  See [`backend/README.md`](./backend/README.md) for required variables (e.g., `GOOGLE_GENAI_API_KEY`, `DATABASE_URL`, etc.).

- **Frontend:**  
  Environment variables are managed via `.env` in `frontend/`.  
  See [`frontend/README.md`](./frontend/README.md) for details.

---

## API Documentation

- **Swagger UI:**  
  Once the backend is running, access [http://localhost:8000/docs](http://localhost:8000/docs) for interactive API documentation.

- **Endpoints:**  
  - `/stories` — Create, retrieve, and manage stories.
  - `/jobs` — Submit and track story generation jobs.

  For detailed schemas and usage, see the backend API docs and [`backend/README.md`](./backend/README.md).

---

## Development & Contribution

- **Backend:**  
  Modular Python codebase using FastAPI, SQLAlchemy, and Pydantic.  
  See [`backend/README.md`](./backend/README.md) for structure and contribution guidelines.

- **Frontend:**  
  Modern React app with Vite, functional components, and hooks.  
  See [`frontend/README.md`](./frontend/README.md) for structure and development notes.

- **Issues & PRs:**  
  Please open issues or pull requests for bugs, improvements, or new features.

---

## References

- [FastAPI Documentation](https://fastapi.tiangolo.com/)
- [SQLAlchemy Documentation](https://docs.sqlalchemy.org/)
- [Pydantic Documentation](https://docs.pydantic.dev/)
- [uv Project Manager](https://github.com/astral-sh/uv)
- [Google GenAI API](https://aistudio.google.com/api-keys)
- [React](https://react.dev/)
- [Vite](https://vitejs.dev/)
- [ESLint](https://eslint.org/)
- [Tech With Tim Tutorial](https://youtu.be/_1P0Uqk50Ps?si=BuDYSWagQn5lsix-)

> **Note:**  
> All creative work in this project is not my own. This repository is solely for tutorial purposes, based on the YouTube tutorial by [Tech With Tim](https://youtu.be/_1P0Uqk50Ps?si=BuDYSWagQn5lsix-).

---

## License

This project will be licensed under the terms described in the [LICENSE](./LICENSE) file. Please review it before using or contributing to this repository.
