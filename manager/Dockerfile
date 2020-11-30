FROM python:latest

COPY config.py .
COPY utils_postgres.py .
COPY __init__.py .
COPY tests_integration.py .
COPY __main__.py .
COPY data.csv .

CMD ["python", "__main__.py"]