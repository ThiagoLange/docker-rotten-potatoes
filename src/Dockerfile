FROM python:latest
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . /app
EXPOSE 5000
CMD ["gunicorn", "--workers=1", "--bind", "0.0.0.0:5000", "-c", "config.py", "app:app"]