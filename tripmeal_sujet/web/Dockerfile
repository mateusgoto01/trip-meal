FROM python:3.7-slim

RUN mkdir /app
WORKDIR /app
COPY requirements.txt /app/
RUN pip install -r requirements.txt

COPY app.py dbconnect.py /app/
COPY ./templates /app/templates
COPY ./static /app/static
COPY LICENSE /app/

RUN chmod -x ./app.py
RUN chmod -x ./dbconnect.py

EXPOSE 3000

CMD ["python3", "app.py"]