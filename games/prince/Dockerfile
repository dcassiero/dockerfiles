FROM dcassiero/em_dosbox-base:1.0

WORKDIR /em-dosbox/src
RUN wget https://devopsny.com/blog/em_dosbox/prince.zip && unzip prince.zip && ./packager.py index prince PRINCE.EXE

EXPOSE 8000

CMD ["python", "-m", "SimpleHTTPServer"]