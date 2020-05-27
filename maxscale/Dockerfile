FROM ubuntu:bionic
RUN apt-get -y update
RUN apt-get -y install binutils wget libedit2 libsqlite3-0 libssl1.0.0
RUN wget https://downloads.mariadb.com/MaxScale/2.2.14/ubuntu/dists/bionic/main/binary-amd64/maxscale-2.2.14-1.ubuntu.bionic.x86_64.deb -O /a.deb
RUN dpkg -i /a.deb
RUN apt-get install -f 
COPY maxscale.cnf /etc/maxscale.cnf
CMD ["maxscale", "-d", "-U", "maxscale", "-l", "stdout"]