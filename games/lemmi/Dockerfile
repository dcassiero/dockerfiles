FROM dcassiero/em_dosbox-base:1.0

WORKDIR /em-dosbox/src
RUN wget https://devopsny.com/blog/em_dosbox/lemmi.zip && unzip lemmi.zip && ./packager.py index lemmi lemvga.com

EXPOSE 8000

CMD ["python", "-m", "SimpleHTTPServer"]