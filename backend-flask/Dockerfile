# Stage 1: Build stage
FROM python:3.10-slim-buster as build

WORKDIR /backend-flask

COPY requirements.txt requirements.txt
RUN pip3 install --no-cache-dir -r requirements.txt

COPY . .

# Stage 2: Final stage
FROM python:3.10-slim-buster

WORKDIR /backend-flask

COPY --from=build /backend-flask .

ENV FLASK_ENV=development
ENV PORT=4567
EXPOSE ${PORT}

CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0"]