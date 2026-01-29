# Torrserver docker image

to run:

docker run \
       --name torrserver \
       -v /root/torrserver/torrserver.data:/app/data  -p 8090:8090 \
       -it -d --cap-drop=ALL --security-opt=no-new-privileges --read-only -u 65534 \
       zamal/torrserver:137
