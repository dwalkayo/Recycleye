FROM amd64/python:3.8

# Install dependencies
RUN mkdir /app 
COPY ./opt/requirements.txt /app
WORKDIR /app
RUN export TMPDIR='/var/tmp' \
   pip install -r ./requirements.txt
COPY ./opt/app /app
#Download coco model and replace saved model in current working directory
WORKDIR /app/model
RUN rm saved_model.pb \
 pip install wget \
 wget http://download.tensorflow.org/models/object_detection/ssd_mobilenet_v1_coco_2018_01_28.tar.gz \
 tar -xvf ssd_mobilenet_v1_coco_2018_01_28.tar.gz ssd_mobilenet_v1_coco_2018_01_28/saved_model/saved_model.pb
WORKDIR /app
EXPOSE 8080
CMD ["python3", "./app.py"]
