FROM jupyter/scipy-notebook:latest

RUN conda install --quiet --yes pytorch torchvision torchaudio cpuonly -c pytorch
RUN conda install --quiet --yes -c conda-forge onnx
RUN python3 -m pip install onnxruntime