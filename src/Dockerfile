FROM python:3-alpine

WORKDIR /app/src
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .

ENTRYPOINT exec gunicorn --bind :$PORT --workers 1 --threads 8 main:app
