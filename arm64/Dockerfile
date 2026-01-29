FROM arm64v8/debian:bookworm-slim
LABEL org.opencontainers.image.authors="zamal@inbox.ru"
ENV HOME=/app       \
    TS_PORT=8090    \
    TS_DONTKILL=1   \
    TS_HTTPAUTH=0

WORKDIR /app
COPY --chown=nobody:nogroup --chmod=700  TorrServer-linux-arm64 /app/torrserver
CMD ["/app/torrserver","--path","/app/data","--torrentsdir","/app/data/torrents"]

# https://github.com/YouROK/TorrServer