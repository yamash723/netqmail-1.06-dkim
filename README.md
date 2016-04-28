# netqmail-1.06-dkim

DKIM patch for netqmail-1.06

# Usage

install `libdkim`

```
wget http://downloads.sourceforge.net/libdkim/libdkim-1.0.19.zip
wget http://www.bltweb.net/qmail/libdkim-1.0.19-linux.patch
wget http://www.bltweb.net/qmail/libdkim-1.0.19-extra-options.patch
unzip libdkim-1.0.19.zip
cd libdkim/src
patch -p2 < ../../libdkim-1.0.19-linux.patch
patch -p2 < ../../libdkim-1.0.19-extra-options.patch
make
make install
```

patch for netqmail

```
wget http://qmail.org/netqmail-1.06.tar.gz
tar zxvf netqmail-1.06.tar.gz
patch -p0 < netqmail-1.06-dkim.patch
make
make man
make setup check
```
