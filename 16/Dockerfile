FROM alpine:3.15

RUN apk add openjdk16

FROM scratch

COPY --from=0 /lib/ld-musl-x86_64.so.1 /lib/ld-musl-x86_64.so.1
COPY --from=0 /lib/libc.musl-x86_64.so.1 /lib/libc.musl-x86_64.so.1
COPY --from=0 /lib/libz.so.1 /lib/libz.so.1

COPY --from=0 /usr/lib/jvm/java-16-openjdk/ /usr/lib/jvm/java-16-openjdk/

CMD ["/usr/lib/jvm/java-16-openjdk/bin/java","-version"]