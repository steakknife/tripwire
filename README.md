# Tripwire open-source

## Build release from source

### Generic

Install C & C++ compiler, make, m4, autoconf, automake, libtool and OpenSSL

```shell
./autogen.sh
./configure
make
```


### Ubuntu

```shell
sudo apt-get install --no-install-recommends build-essential libssl-dev
./autogen.sh
./configure --disable-dependency-tracking --disable-debug
make
```


### FreeBSD

```shell
[su | sudo] pkg install openssl m4 libtool autoconf automake
./autogen.sh
./configure --disable-dependency-tracking --disable-debug --with-ssl-dir=/usr/local
make
```


### OSX

#### Homebrew

TODO: brew formula

```shell
brew install openssl m4 libtool autoconf automake
./autogen.sh
./configure CXXFLAGS='-stdlib=libstdc++' --disable-dependency-tracking --disable-debug --with-ssl-dir=/usr/local
make
```


## Cleanup between builds

    ./clean

## Tested platforms

- Ubuntu LTS latest
- FreeBSD latest
- OSX latest
