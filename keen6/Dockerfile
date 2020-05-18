FROM dcassiero/em_dosbox-base:1.0

WORKDIR /em-dosbox/src
RUN wget https://devopsny.com/blog/em_dosbox/keen6.zip && unzip keen6.zip && ./packager.py index keen6 keen6.exe

EXPOSE 8000

CMD ["python", "-m", "SimpleHTTPServer"]