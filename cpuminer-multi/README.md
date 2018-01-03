*Be sure you installed Docker in your machine. If not, please visit [here](https://github.com/tuanphung/miner-dockerfile/blob/master/README.md) first.*

Open your terminal, and follow these commands.

1. `docker build - t cpuminer-multi .`

2. `docker run -it cpuminer-multi -a cryptonight -o stratum+tcp://<pool address>:<pool port> -u <Your Electroneum Public Wallet> -p x -t 7`

`-a`: hash algorithm (it's *cryptonight* for ETN)

`-o`: pool

`-u`: wallet address

`-p`: password. In case you're using Electroneum public address, just leave password as *x*

`-t`: number of threads you want to start (optional)
