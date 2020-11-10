FROM tensorflow/tensorflow:1.15.4-gpu-py3-jupyter

RUN rm -r /tf && mkdir /tf
WORKDIR /tf

COPY ./requirements.txt /tf/requirements.txt
RUN pip3 install -r requirements.txt