FROM dcassiero/em_dosbox-base:1.0

WORKDIR /em-dosbox/src
RUN wget https://devopsny.com/blog/em_dosbox/lodetlr.zip && unzip lodetlr.zip && ./packager.py index lodetlr LR.BAT

EXPOSE 8000

CMD ["python", "-m", "SimpleHTTPServer"]