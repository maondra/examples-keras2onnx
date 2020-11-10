# Pytorch to onnx (Export)

### Steps

* Build docker container
   * docker build --tag=pytorch2onnx .
* Run docker
  * docker run --rm -v <PATH_TO_THIS_FOLDER>:/home/jovyan/work -p 8888:8888 pytorch2onnx:latest
* Open "pytorch_Export_to_onnx.ipynb" notebook
* Follow the instructions