# Etapa de construcción 
FROM python:3.9-slim AS builder

WORKDIR /build

COPY requirements.txt .

RUN pip install -r requirements.txt

COPY . .


FROM alpine:3.14 AS production

WORKDIR /app

COPY --from=builder /build /app

CMD ["bin/bash"]

