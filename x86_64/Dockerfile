FROM alpine AS downloader
ARG TORRSERVER_VERSION="144.1"
USER nobody
WORKDIR /app
RUN wget https://github.com/YouROK/TorrServer/releases/download/MatriX.${TORRSERVER_VERSION}/TorrServer-linux-amd64 -O /app/torrserver && \
    chmod 777 /app/torrserver


FROM debian:trixie-slim
LABEL org.opencontainers.image.authors="zamal@inbox.ru"
ENV HOME=/app       \
    TS_PORT=8090    \
    TS_DONTKILL=1   \
    TS_HTTPAUTH=0
COPY --from=downloader --chown=nobody:nogroup /app /app
RUN chmod -R -s /usr/bin/* /usr/sbin/* # fix CIS-DI-0008
USER nobody
WORKDIR /app
CMD ["/app/torrserver","--path","/app/data","--torrentsdir","/app/data/torrents"]

