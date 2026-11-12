ARG BUILD_FROM
FROM $BUILD_FROM

COPY rootfs /

RUN apk add --no-cache git \
    && pip install --no-cache-dir "git+https://github.com/bla3e316/bluetti_mqtt.git" \
    && chmod a+x /run.sh

CMD [ "/run.sh" ]
