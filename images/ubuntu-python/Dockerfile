FROM ubuntu

RUN apt update && apt install python3 -y && apt clean

COPY app.py /opt/app.py

CMD python3 /opt/app.py


