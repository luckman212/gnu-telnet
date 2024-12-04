# gnu-telnet

## What is this?

This is an x86-64 build of `telnet` for macOS.

It was compiled on my Mac Mini M4 from the GPG-verified inetutils 2.5 source (https://ftp.gnu.org/gnu/inetutils/inetutils-2.5.tar.xz) on 2024-12-03 using the following commands:

```
$ ./configure --prefix=/usr/local/inetutils-x86 \
            --disable-syslogd \
            --enable-telnet \
            CC="clang" \
            CFLAGS="-arch x86_64"

$ make clean

$ make
```

## What the heck? It's 2024, why would I need telnet?

I don't know. This was compiled specifically to troubleshoot the issue described at https://apple.stackexchange.com/questions/476182/some-programs-report-no-route-to-host-connecting-to-servers-when-run-without-s. If you aren't experiencing that problem, you don't need this.

## Instructions

1. Download the `telnet_x86.tar.gz` archive from the [releases][1] page
2. Extract it by double-clicking
3. Remove the `quarantine` flag:
```
xattr -d com.apple.quarantine ~/Downloads/telnet
```
4. Copy or move that `telnet` binary to `/usr/local/bin`
5. From a Terminal, run `telnet -V` to check if it was installed correctly.

[1]: https://github.com/luckman212/gnu-telnet/releases/
