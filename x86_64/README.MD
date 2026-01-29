# Torrserver docker image

to run:

docker run \\\n
       --name torrserver \\\n
       -p 8090:8090 \\\n
       -v /root/torrserver/torrserver.data:/app/data  \\\n
       -it -d --cap-drop=ALL --security-opt=no-new-privileges --read-only -u 65534 \\\n
       zamal/torrserver:137
