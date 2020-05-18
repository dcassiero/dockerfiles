FROM dcassiero/em_dosbox-base:1.0

WORKDIR /em-dosbox/src
RUN wget https://devopsny.com/blog/em_dosbox/sq1.zip && unzip sq1.zip && ./packager.py index sq1 SQ.COM

EXPOSE 8000

CMD ["python", "-m", "SimpleHTTPServer"]