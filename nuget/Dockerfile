FROM alpine:3.8

RUN apk update
RUN apk add mono -X http://dl-cdn.alpinelinux.org/alpine/edge/testing/

RUN wget -P /usr/lib/mono https://dist.nuget.org/win-x86-commandline/latest/nuget.exe \
    && echo -e '#!/bin/sh\nexec /usr/bin/mono $MONO_OPTIONS /usr/lib/mono/nuget.exe "$@"' > /usr/bin/nuget \
    && chmod a+x /usr/bin/nuget \
    && nuget

RUN apk add --no-cache ca-certificates && cert-sync /etc/ssl/certs/ca-certificates.crt