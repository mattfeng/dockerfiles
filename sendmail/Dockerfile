FROM debian:buster

RUN sudo apt-get update && sudo apt-get -y upgrade
RUN sudo apt-get install -y sendmail

EXPOSE 25

ENTRYPOINT ["sleep"]
CMD ["infinity"]
