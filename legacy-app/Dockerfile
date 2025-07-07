FROM python:3.9-slim AS builder

WORKDIR /build

# Instalo las dependencias necesarias
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY . .

FROM python:3.9-slim as production
WORKDIR /app

COPY --from=builder /build /app

CMD ["python3"]