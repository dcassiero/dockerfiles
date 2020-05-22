FROM dcassiero/em_dosbox-base:1.0

WORKDIR /em-dosbox/src
RUN wget https://devopsny.com/blog/em_dosbox/gta.zip && unzip gta.zip && ./packager.py index gta gtados.bat

EXPOSE 8000

CMD ["python", "-m", "SimpleHTTPServer"]