FROM dcassiero/em_dosbox-base:1.0

WORKDIR /em-dosbox/src
RUN wget https://devopsny.com/blog/em_dosbox/simearth.zip && unzip simearth.zip && ./packager.py index simearth SIMEARTH.EXE

EXPOSE 8000

CMD ["python", "-m", "SimpleHTTPServer"]