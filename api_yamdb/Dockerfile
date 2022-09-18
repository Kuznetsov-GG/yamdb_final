FROM python:3.7-slim
COPY ./ /app
RUN pip install -r /app/requirements.txt
WORKDIR /app/infra_project/
CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000" ]