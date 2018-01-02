#
# ex: docker run cpuminer-multi -o stratum+tcp://ltc.pool.com:80 -u creack.worker1 -p xxx -t 7
#

FROM		ubuntu:latest

RUN		apt-get update -qq

RUN		apt-get install -qqy automake
RUN		apt-get install -qqy libcurl4-openssl-dev
RUN		apt-get install -qqy git
RUN		apt-get install -qqy make
RUN		apt-get install -y build-essential

RUN		git clone https://github.com/OhGodAPet/cpuminer-multi

RUN		cd cpuminer-multi && ./autogen.sh
RUN		cd cpuminer-multi && ./configure CFLAGS="-O3"
RUN		cd cpuminer-multi && make

WORKDIR		/cpuminer-multi
ENTRYPOINT	["./minerd"]
