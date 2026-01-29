# TorrServer docker image for arm64

to build:
<pre>
TORRSERVER_VERSION="137"
wget https://github.com/YouROK/TorrServer/releases/download/MatriX.${TORRSERVER_VERSION}/TorrServer-linux-arm64
chmod 700 TorrServer-linux-arm64
docker build --platform arm64 --tag zamal/torrserver:${TORRSERVER_VERSION}-arm64 .
rm -f TorrServer-linux-arm64
</pre>