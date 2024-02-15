FROM python:3.8-buster

MAINTAINER Sebastien Siddi (sebastien.siddi@gmail.com)

WORKDIR /

RUN pip install --upgrade pip

RUN apt-get update && apt-get install -y libldap2-dev libsasl2-dev && rm -rf /var/lib/apt/lists/*

COPY student_age.py .

COPY requirements.txt .

RUN pip3 install -r /requirements.txt

VOLUME ["/data"]

EXPOSE 5000

CMD [ "python", "./student_age.py" ]
