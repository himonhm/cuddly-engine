FROM mcr.microsoft.com/devcontainers/python:1-3.11-bullseye

WORKDIR /workspaces

RUN pip install --upgrade pip "poetry==1.5.1"
RUN poetry config virtualenvs.create false --local
COPY ./backend/pyproject.toml  ./backend/poetry.lock ./
RUN poetry install 