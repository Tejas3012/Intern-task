FROM python:3.11-slim

WORKDIR /app

COPY pyproject.toml uv.lock ./

# Install uvicorn and project dependencies
RUN pip install --upgrade pip && pip install uvicorn flask

COPY . .

EXPOSE 5000

CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "5000"]

