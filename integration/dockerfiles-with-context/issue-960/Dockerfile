FROM alpine:3.14 as rootfs
RUN echo 7777

FROM alpine:3.14
COPY --from=rootfs / /sysroot/
