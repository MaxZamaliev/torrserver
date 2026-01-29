# Torrserver docker image

to run:
<pre>
docker run \
       --name torrserver \
       -p 8090:8090 \
       -v /root/torrserver/torrserver.data:/app/data  \
       -it -d --cap-drop=ALL --security-opt=no-new-privileges --read-only -u 65534 \
       zamal/torrserver:137
</pre>
