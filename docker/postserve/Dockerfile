FROM osgeo/proj:6.2.1
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

VOLUME /mapping

RUN apt-get update && apt-get install -y python3 python3-pip libpq-dev

COPY . /usr/src/app/
RUN pip3 install --no-cache-dir -r requirements.txt

CMD ["python3", "-u","/usr/src/app/server.py"] 
