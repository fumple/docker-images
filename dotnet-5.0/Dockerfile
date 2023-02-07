# Credit to https://pterodactyl.io/community/config/eggs/creating_a_custom_image.html
FROM mcr.microsoft.com/dotnet/runtime:5.0

MAINTAINER Fumple, <me@fumple.pl>

RUN apk add --no-cache --update curl ca-certificates openssl git tar bash sqlite fontconfig \
    && adduser --disabled-password --home /home/container container

USER container
ENV  USER=container HOME=/home/container

WORKDIR /home/container

COPY ./entrypoint.sh /entrypoint.sh

CMD ["/bin/bash", "/entrypoint.sh"]
