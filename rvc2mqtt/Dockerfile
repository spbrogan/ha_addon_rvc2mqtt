# https://developers.home-assistant.io/docs/add-ons/configuration#add-on-dockerfile
ARG BUILD_FROM
FROM $BUILD_FROM

COPY ./default_config.yaml .

COPY rootfs /


RUN apk add --no-cache python3 py3-pip git
RUN pip3 install --no-cache-dir git+https://github.com/spbrogan/rvc2mqtt.git@main_split#egg=rvc2mqtt
