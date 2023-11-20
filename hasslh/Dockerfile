ARG BUILD_FROM
FROM $BUILD_FROM

## Execute during the build of the image
#ARG TEMPIO_VERSION BUILD_ARCH
#RUN \
#    curl -sSLf -o /usr/bin/tempio \
#    "https://github.com/home-assistant/tempio/releases/download/${TEMPIO_VERSION}/tempio_${BUILD_ARCH}"

RUN apk add --no-cache --repository http://dl-3.alpinelinux.org/alpine/edge/testing/ sslh

# Copy root filesystem
COPY rootfs /
# Fix permission
RUN chmod +x /etc/services.d/hasslh/run
RUN chmod +x /etc/services.d/hasslh/finish
RUN chmod +x /usr/bin/my_program

