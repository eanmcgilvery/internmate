FROM ubuntu

RUN apt-get update -y && \
    apt-get install -y python3-pip python3-dev libmysqlclient-dev libssl-dev libffi-dev

COPY ./requirements.txt /app/requirements.txt

WORKDIR /app

RUN pip3 install -r requirements.txt && apt-get install -y curl
ENV CHAT_PASS IgEIq2oqa4EHNZtd0KHQLs9Pm6bwLDwE 
ENV CHAT_IP 172.18.0.5
ENV SECRET_KEY internmate-app-demo
COPY ./app /app

ENTRYPOINT ["python3"]

CMD ["main.py"]
