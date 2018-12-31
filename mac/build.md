```
brew install pkg-config

```

# openssl
```

git clone git@github.com:openssl/openssl.git
cd openssl
git checkout OpenSSL_1_0_2j 

CC="cc -mmacosx-version-min=10.8 " ./Configure darwin64-x86_64-cc --prefix="$(pwd)/../libs" no-shared

make
make istall -j16
```

# libevent

```
git clone git@github.com:libevent/libevent.git
cd libevent
./autogen.sh

# no open ssl
./configure  CFLAGS=" -mmacosx-version-min=10.8  "  --disable-shared --disable-openssl --enable-static --disable-debug-mode  --disable-clock-gettime  --prefix="$(pwd)/../libs"

# with open ssl
PKG_CONFIG_PATH="$(pwd)/../libs/lib/pkgdir" ./configure CFLAGS=" -mmacosx-version-min=10.8  -I\"$(pwd)/../libs/include\" "  LDFLAGS="-L\"$(pwd)/../libs/lib\" "  --disable-shared  --enable-static --disable-debug-mode  --disable-clock-gettime  --prefix="$(pwd)/../libs"

make
make install
```
