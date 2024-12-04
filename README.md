# gnu-telnet

This is an x86-64 build of `telnet`.

It was compiled from the inetutils 2.5 source (https://ftp.gnu.org/gnu/inetutils/inetutils-2.5.tar.xz) on 2024-12-03 using the following commands:

```
$ ./configure --prefix=/usr/local/inetutils-x86 \
            --disable-syslogd \
            --enable-telnet \
            CC="clang" \
            CFLAGS="-arch x86_64"

$ make clean

$ make
```

