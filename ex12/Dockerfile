FROM python:3.12-slim-bookworm

RUN adduser --disabled-password appuser

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir --upgrade pip && \
	pip install --no-cache-dir -r requirements.txt

COPY . .

RUN chown -R appuser:appuser /app
USER appuser

CMD ["python", "app.py"]
