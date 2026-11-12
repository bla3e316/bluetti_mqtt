ARG BUILD_FROM
FROM $BUILD_FROM

# Supervisor passes the add-on version. Using it in the RUN below changes the
# layer whenever the version is bumped, so pip re-fetches the library instead
# of reusing a cached copy of an older commit.
ARG BUILD_VERSION

COPY rootfs /

RUN echo "Installing bluetti_mqtt for add-on ${BUILD_VERSION}" \
    && apk add --no-cache git \
    && pip install --no-cache-dir "git+https://github.com/bla3e316/bluetti_mqtt.git" \
    && chmod a+x /run.sh

CMD [ "/run.sh" ]
