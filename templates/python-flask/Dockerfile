FROM python:3.6-slim
WORKDIR /usr/local/lib/python3.6/site-packages
COPY ./requirements/. .
WORKDIR /app
COPY ./main.py .
EXPOSE 5000
CMD ["python", "main.py"]
