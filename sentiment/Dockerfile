FROM python:3.11-slim

ENV PYTHONUNBUFFERED 1
ENV PYTHONDONTWRITEBYTECODE 1

WORKDIR /sentiment

RUN apt-get update && apt-get install -y \
    libpq-dev \
    gcc \
    && rm -rf /var/lib/apt/lists/*

COPY requirements.txt /sentiment/

RUN pip install --upgrade pip && pip install --no-cache-dir -r requirements.txt

COPY . /sentiment/

EXPOSE 5000

CMD ["echo", "Placeholder"]