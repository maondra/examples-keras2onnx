FROM nvcr.io/nvidia/tensorrt:20.10-py3

RUN apt-get update && apt-get install autoconf automake libtool curl make g++ unzip -y

WORKDIR /protobuf
RUN git clone https://github.com/google/protobuf.git
RUN ls
WORKDIR /protobuf/protobuf
RUN git submodule update --init --recursive
RUN ./autogen.sh
RUN ./configure
RUN make
RUN make check
RUN make install
RUN ldconfig

#install onnx2trt
WORKDIR /onnx2trt
RUN git clone https://github.com/onnx/onnx-tensorrt.git 
WORKDIR /onnx2trt/onnx-tensorrt
RUN git submodule update --init --recursive
RUN mkdir build
WORKDIR /onnx2trt/onnx-tensorrt/build
RUN cmake .. -DTENSORRT_ROOT=/opt/tensorrt/ && make -j8
ENV LD_LIBRARY_PATH=$PWD:$LD_LIBRARY_PATH