FROM ubuntu:18.04

RUN apt-get update && apt-get -y upgrade
RUN apt-get install -y openssl libssl-dev vim sasl2-bin dnsutils
RUN apt-get install -y sendmail

# logs
# /var/mail

# installing and configuring sendmail
# source: https://tecadmin.net/install-sendmail-on-debian-9-stretch/
# source: https://archive.is/fRgpB

# edit /etc/mail/sendmail.mc
# define(`confDOMAIN_NAME', `thedevelopingdev.com')
# source: https://archive.is/kkDwJ

# set valid hostname: --hostname="host.local"

EXPOSE 25

ENTRYPOINT ["sleep"]
CMD ["infinity"]
