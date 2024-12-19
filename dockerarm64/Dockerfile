FROM alpine:latest

# set version label
ARG BUILD_DATE
ARG VERSION
ARG MISSARR_VERSION
LABEL build_version="Local version:- ${VERSION} Build-date:- ${BUILD_DATE}"
LABEL maintainer="myhme"

RUN apk add tzdata
ADD https://github.com/myhme/missarr/releases/download/${MISSARR_VERSION}/missarr_${MISSARR_VERSION}_linux_arm64 /opt/missarr/missarr
RUN chmod +x /opt/missarr/missarr
WORKDIR "/opt/missarr"
VOLUME /opt
ENTRYPOINT ["tail","-f"]