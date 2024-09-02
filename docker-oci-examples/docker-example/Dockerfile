From centos:latest

RUN apt-get update
RUN apt-get upgrade -y

RUN apt-get install clang -y
RUN apt-get install cmake -y
RUN apt-get install git -y
RUN apt-get install curl -y
RUN apt-get install zip -y
RUN apt-get install gdb -y
RUN apt-get install pkg-config -y
RUN apt-get install libsdl2-dev -y
RUN apt install libsdl2-2.0-0 -y
RUN apt install libsdl2-image-dev -y
RUN apt install libsdl2-mixer-dev -y
RUN apt install libsdl2-ttf-dev -y
RUN apt install ninja-build

ARG VCPKG_FORCE_SYSTEM_BINARIES=1

RUN git clone --depth 1 https://github.com/microsoft/vcpkg
RUN ./vcpkg/bootstrap-vcpkg.sh
ENV VCPKG_DEFAULT_TRIPLET=x64-mingw-dynamic
ENV VCPKG_DEFAULT_HOST_TRIPLET=x64-mingw-dynamic

RUN /vcpkg/vcpkg install grpc
RUN /vcpkg/vcpkg install nlohmann-json
RUN /vcpkg/vcpkg install sdl2
RUN /vcpkg/vcpkg install sdl2pp
RUN /vcpkg/vcpkg install sdl2-mixer
RUN /vcpkg/vcpkg install sdl2-ttf
RUN /vcpkg/vcpkg install sld2-image
RUN /vcpkg/vcpkg install sdl2-gfx
