FROM alpine

RUN apk update && \
    apk add --no-cache bind-tools dnsmasq openrc

COPY entrypoint.sh /
RUN chmod +x /entrypoint.sh
RUN rc-update add dnsmasq
COPY dnsmasq/ /etc

ENTRYPOINT ["/entrypoint.sh"]
