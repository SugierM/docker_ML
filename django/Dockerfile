FROM python:3.11-slim

ENV PYTHONUNBUFFERED 1
ENV PYTHONDONTWRITEBYTECODE 1

WORKDIR /ui_django

# Install system dependencies
RUN apt-get update && apt-get install -y \
    libpq-dev \
    gcc \
    && rm -rf /var/lib/apt/lists/*

# Install Python dependencies
COPY requirements.txt /ui_django/

RUN pip install --upgrade pip && pip install --no-cache-dir -r requirements.txt

COPY . /ui_django/

EXPOSE 8000

RUN python manage.py migrate
# Run migrations and collectstatic (if needed)
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
