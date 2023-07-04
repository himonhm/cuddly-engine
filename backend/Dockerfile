FROM python:3.11

ENV PYTHONUNBUFFERED=1

WORKDIR /app

RUN pip install --upgrade pip "poetry==1.5.1"
RUN poetry config virtualenvs.create false --local
COPY backend/pyproject.toml backend/poetry.lock ./
RUN poetry install 

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]