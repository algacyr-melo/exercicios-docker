FROM python:3.11-slim

RUN addgroup --system appgroup && \
	adduser --system --no-create-home --ingroup appgroup appuser

RUN apt-get update && apt-get install -y --no-install-recommends \
	gcc \
	libc-dev \
	&& rm -rf /var/lib/apt/lists/*

RUN mkdir /app && chown appuser:appgroup /app
WORKDIR /app

COPY --chown=appuser:appgroup requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY --chown=appuser:appgroup . .

USER appuser

EXPOSE 5000

CMD ["python", "app.py"]
