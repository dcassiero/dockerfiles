FROM dcassiero/em_dosbox-base:1.0

WORKDIR /em-dosbox/src
RUN wget https://devopsny.com/blog/em_dosbox/mlbb.zip && unzip mlbb.zip && ./packager.py index mlbb Mlbb.com

EXPOSE 8000

CMD ["python", "-m", "SimpleHTTPServer"]