FROM dcassiero/em_dosbox-base:1.0

WORKDIR /em-dosbox/src
RUN wget https://devopsny.com/blog/em_dosbox/civ.zip && unzip civ.zip && ./packager.py index civ CIV.BAT

EXPOSE 8000

CMD ["python", "-m", "SimpleHTTPServer"]