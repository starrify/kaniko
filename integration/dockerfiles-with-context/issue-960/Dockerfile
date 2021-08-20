FROM alpine:3.14 as rootfs
RUN echo 7777
RUN rm -f /var/run \
 && mkdir -p /var/run/foo \
 && touch /var/run/foo/bar

FROM alpine:3.14
COPY --from=rootfs / /sysroot/
RUN find /sysroot/dev/ /sysroot/sys/ /sysroot/var/run/ -mindepth 1 > /tmp/list \
 && ! grep . /tmp/list
