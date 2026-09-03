# Torrserver docker image

to build:
<pre>
TORRSERVER_VERSION=144.1
docker build --tag zamal/torrserver:${TORRSERVER_VERSION} --build-arg TORRSERVER_VERSION=${TORRSERVER_VERSION} .
</pre>


to run:
<pre>
docker run \
       --name torrserver \
       -p 8090:8090 \
       -v /root/torrserver/torrserver.data:/app/data  \
       -it -d --cap-drop=ALL --security-opt=no-new-privileges --read-only -u 65534 \
       zamal/torrserver:144.1
</pre>
