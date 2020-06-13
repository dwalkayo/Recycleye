#FROM ubuntu:16.04
FROM amd64/python:latest

# Install dependencies
RUN mkdir /app 
#WORKDIR /app
COPY ./opt/requirements.txt /app
#RUN wget -O /app/ssd_mobilenet_v1_coco_2018_01_28.tar.gz http://download.tensorflow.org/models/object_detection/ssd_mobilenet_v1_coco_2018_01_28.tar.gz
#RUN tar -xvf ssd_mobilenet_v1_coco_2018_01_28.tar.gz ssd_mobilenet_v1_coco_2018_01_28/saved_model/saved_model.pb
WORKDIR /app
#RUN apt-get update && apt-get install -y \
#    software-properties-common
#RUN add-apt-repository universe
#RUN apt-get update && apt-get install -y \
#    python-pip \
#    python
#RUN pip freeze > requirements.txt
RUN pip install -r ./requirements.txt
#RUN pip3 freeze > requirements.txt
#RUN apk add --update nodejs nodejs-npm
COPY ./opt/app /app
WORKDIR /app/model
#RUN rm saved_model.pb
#RUN pip install wget
#RUN wget http://download.tensorflow.org/models/object_detection/ssd_mobilenet_v1_coco_2018_01_28.tar.gz
#RUN tar -xvf ssd_mobilenet_v1_coco_2018_01_28.tar.gz ssd_mobilenet_v1_coco_2018_01_28/saved_model/saved_model.pb
WORKDIR /app
EXPOSE 8080
CMD ["python3", "./app.py"]
