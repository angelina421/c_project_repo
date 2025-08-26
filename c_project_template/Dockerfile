FROM ubuntu

WORKDIR /usr/src/cpp

ENV DEBIAN_FRONTEND=noninteractive

# 安装编译环境
RUN apt update
RUN apt install -y build-essential

# 复制整个 src 文件夹
COPY  src/ ./src/

# 直接编译
# 编译 src 下的所有 .cpp 文件
RUN g++ src/*.cpp -o main

# 用 Makefile
# WORKDIR /usr/src/cpp/src
# RUN make

# 用 CMake
# WORKDIR /usr/src/cpp/build
# RUN cmake ../src && make

# 运行程序
CMD ["./main"] 