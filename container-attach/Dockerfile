FROM python:alpine 

COPY app.py .
COPY requirements.txt .

RUN pip install -r requirements.txt

ENTRYPOINT ["python3"]

CMD ["app.py"]