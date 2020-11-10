# Keras model to ONNX (Conversion)

### Steps

* Build docker container
   * docker build --tag=keras2onnx:0.0.0 -f Dockerfile .
* Run docker
  * docker run --rm -v <YOUR_PATH>:/tf -p 8888:8888 keras2onnx:0.0.0
* Open "Keras2ONNX.ipynb" notebook
* Follow the instructions