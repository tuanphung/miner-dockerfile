#
# ex: docker run -it cpuminer-multi -a cryptonight -o stratum+tcp://etn-us-west1.nanopool.org:13333 -u etnjwDgV1DzN9Be1ByAXE2aEZBX2DPpF3XdHt5PSqWrPTbGSjPbxbDK3yGRzc29i9MUe3RYvubSxkRaeZCey5aZP47jTf22yK8.worker/email
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
