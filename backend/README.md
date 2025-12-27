# Interactive Story Generator AI Backend

This is the backend for the **Story Generator** project, built with Python and FastAPI. It provides RESTful APIs for generating, storing, and managing stories and jobs. The backend is modular, leveraging FastAPI, SQLAlchemy, and Pydantic for robust and scalable development. Project management and dependency handling are streamlined using [uv](https://github.com/astral-sh/uv).

---

## Table of Contents

- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [API Overview](#api-overview)
- [Reference](#reference)

---

## Features

- Story generation via customizable prompts
- LLM (Large Language Model) integration for advanced text generation
- Job management for asynchronous processing
- RESTful API endpoints for stories and jobs
- Modular codebase with clear separation of concerns
- Environment-based configuration
- Database integration with SQLAlchemy

---

## Project Structure

```
backend/
│
├── core/           # Core logic: config, models, prompts, story generation
│   ├── config.py
│   ├── models.py
│   ├── prompts.py
│   └── story_generator.py
│
├── db/             # Database setup and connection
│   └── database.py
│
├── models/         # ORM models
│   ├── job.py
│   └── story.py
│
├── routers/        # API routers
│   ├── job.py
│   └── story.py
│
├── schemas/        # Pydantic schemas for validation
│   ├── job.py
│   └── story.py
│
├── main.py         # FastAPI application entry point
├── requirements.txt
├── pyproject.toml
├── .env            # Environment variables
└── README.md
```

---

## Installation

This project uses [uv](https://github.com/astral-sh/uv) for Python project management and dependency resolution.

1. **Install uv:**
    ```bash
    pip install uv
    ```

2. **Create a virtual environment:**
    ```bash
    uv venv
    ```

3. **Activate the virtual environment:**
    - On Unix/macOS:
      ```bash
      source .venv/bin/activate
      ```
    - On Windows:
      ```bash
      .venv\Scripts\activate
      ```

4. **Sync dependencies:**
    ```bash
    uv sync
    ```

---

## Configuration

1. **Create a `.env` file in the `backend/` directory.**
2. **Add the following environment variables to the `.env` file:**
    ```
    # Google GenAI API Key
    GOOGLE_GENAI_API_KEY=your_api_key_here

    # Database URL
    DATABASE_URL=sqlite:///./database.db

    # API Prefix
    API_PREFIX=/api

    # Debug mode
    DEBUG=True

    # Allowed CORS origins (comma-separated)
    ALLOWED_ORIGINS=https://localhost:3000, https://localhost:5173
    ```
3. **Adjust other settings in `core/config.py` as needed (e.g., database URL, secret keys, etc.).**

---

## Usage

1. **Run the FastAPI server:**
    ```bash
    cd backend
    uv run main.py
    ```

2. **Access the API docs:**
    - Open [http://localhost:8000/docs](http://localhost:8000/docs) for Swagger UI.

---

## API Overview

- **/stories**: Create, retrieve, and manage stories.
- **/jobs**: Submit and track story generation jobs.

Refer to the auto-generated docs at `/docs` for detailed endpoints and schemas.

---


## Reference

> **Note:**  
> All creative work in this project is not my own. This repository is solely for tutorial purposes, based on the YouTube tutorial by [Tech With Tim](https://youtu.be/_1P0Uqk50Ps?si=BuDYSWagQn5lsix-).


- [FastAPI Documentation](https://fastapi.tiangolo.com/)
- [SQLAlchemy Documentation](https://docs.sqlalchemy.org/)
- [Pydantic Documentation](https://docs.pydantic.dev/)
- [uv Project Manager](https://github.com/astral-sh/uv)
- [Google GenAI API](https://aistudio.google.com/api-keys)

