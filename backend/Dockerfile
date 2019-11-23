FROM python:3.7

RUN pip install fastapi uvicorn

EXPOSE 80

COPY ./app /app

HEALTHCHECK --interval=5s --timeout=3s --retries=3 CMD curl -f http://localhost:80 || exit 1

CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "80"]
