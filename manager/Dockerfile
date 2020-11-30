FROM python:latest

COPY config.py .
COPY utils_postgres.py .
COPY __init__.py .
COPY tests_integration.py .
COPY __main__.py .
COPY data.csv .
COPY requirements.txt .

RUN pip install -r requirements.txt

EXPOSE 5432
EXPOSE 5000

RUN wget https://raw.githubusercontent.com/vishnubob/wait-for-it/master/wait-for-it.sh -P /
RUN chmod +x /wait-for-it.sh
ENTRYPOINT ["/wait-for-it.sh", "db:5432", "--"]

CMD ["python", "__main__.py"]