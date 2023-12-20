# Dgbminer
A Digibyte optimized cpu miner. Sha256d, Scrypt, Skein, Qubit and Odocrypt.

# Build for Linux

sudo apt-get install build-essential automake libssl-dev libcurl4-openssl-dev lib32z1-dev libjansson-dev libgmp-dev git

git clone https://github.com/Jongjan88/dgbminer/

cd dgbminer

chmod +x *.sh

./build.sh

#------------------------------------------------------------------

# Run node && cpuminer on the same server!
# Linux Solo - sha256d
./cpuminer -a sha256d -o http://127.0.0.1:14022/ --userpass=user:pass --no-getwork --no-stratum --coinbase-addr=dgbt1q2fz5ckzq7dqvfpz6m2y4k98nw698kdykv8e0ha -D

# Linux Solo - scrypt
./cpuminer -a scrypt -o http://127.0.0.1:14022/ --userpass=user:pass --no-getwork --no-stratum --coinbase-addr=dgbt1q2fz5ckzq7dqvfpz6m2y4k98nw698kdykv8e0ha -D

# Linux Solo - skein
./cpuminer -a skein -o http://127.0.0.1:14022/ --userpass=user:pass --no-getwork --no-stratum --coinbase-addr=dgbt1q2fz5ckzq7dqvfpz6m2y4k98nw698kdykv8e0ha -D

# Linux Solo - qubit
./cpuminer -a qubit -o http://127.0.0.1:14022/ --userpass=user:pass --no-getwork --no-stratum --coinbase-addr=dgbt1q2fz5ckzq7dqvfpz6m2y4k98nw698kdykv8e0ha -D

# Linux Solo - odo
./cpuminer -a odo -o http://127.0.0.1:14022/ --userpass=user:pass --no-getwork --no-stratum --coinbase-addr=dgbt1q2fz5ckzq7dqvfpz6m2y4k98nw698kdykv8e0ha -D

#------------------------------------------------------------------

# Help

./cpuminer --help

# Missing libraries?

libgmp3-dev zlib1g-dev

# Mainnet config ( digibyte.conf )

maxconnections=300
listen=1
server=1
rpcuser=user
rpcpassword=pass
rpcallowip=0.0.0.0
rpcport=14022

# Testnet config ( digibyte.conf )

maxconnections=300
testnet=1
listen=1
server=1

[test]
rpcuser=user
rpcpassword=pass
rpcallowip=0.0.0.0
rpcport=14022
