FROM debian:buster

RUN apt-get update && apt-get install -y \
    python \
	cmake \
	default-jre \
	git-core \
	autotools-dev \
	automake \
	wget \
	unzip \
 && rm -rf /var/lib/apt/lists/*

RUN git clone https://github.com/dcassiero/emsdk.git
WORKDIR /emsdk
RUN ./emsdk install 1.38.43-fastcomp && ./emsdk activate 1.38.43-fastcomp
ENV PATH=/emsdk:/emsdk/fastcomp/emscripten:/emsdk/node/12.9.1_64bit/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
ENV EMSDK=/emsdk
ENV EM_CONFIG=/root/.emscripten
ENV EMSDK_NODE=/emsdk/node/12.9.1_64bit/bin/node
RUN emcc -v

WORKDIR /

RUN git clone -b get-it-working https://github.com/dcassiero/em-dosbox.git
WORKDIR /em-dosbox
RUN ./autogen.sh && emconfigure ./configure --enable-wasm --disable-sync && make

WORKDIR /em-dosbox/src
RUN wget https://devopsny.com/blog/em_dosbox/doom.zip && unzip doom.zip && ./packager.py index doom DOOM.EXE

EXPOSE 8000

CMD ["python", "-m", "SimpleHTTPServer"]
