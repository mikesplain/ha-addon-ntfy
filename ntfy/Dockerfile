ARG NTFY_VERSION BUILD_FROM
FROM binwiederhier/ntfy:${NTFY_VERSION}

# https://developers.home-assistant.io/docs/add-ons/configuration#add-on-dockerfile
FROM $BUILD_FROM

# Execute during the build of the image
# ARG NTFY_VERSION BUILD_ARCH
# RUN \
#     curl -sSLf -o /usr/bin/tempio \
#     "https://github.com/home-assistant/tempio/releases/download/${TEMPIO_VERSION}/tempio_${BUILD_ARCH}"

COPY --from=0 /usr/bin/ntfy /usr/bin/ntfy

# Copy root filesystem
COPY rootfs /


# https://developers.home-assistant.io/docs/add-ons/configuration#add-on-dockerfile
# ARG BUILD_FROM
# FROM $BUILD_FROM

# # Execute during the build of the image
# ARG TEMPIO_VERSION BUILD_ARCH
# RUN \
#     curl -sSLf -o /usr/bin/tempio \
#     "https://github.com/home-assistant/tempio/releases/download/${TEMPIO_VERSION}/tempio_${BUILD_ARCH}"

# # Copy root filesystem
# COPY rootfs /