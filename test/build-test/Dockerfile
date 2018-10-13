FROM alpine

RUN apk update && \
    apk add --no-cache bind-tools dnsmasq

COPY entrypoint.sh /
RUN chmod +x /entrypoint.sh
COPY dnsmasq/ /etc

ENTRYPOINT ["/entrypoint.sh"]
