FROM my_xcaddy AS builder

RUN xcaddy build \
    --with github.com/greenpau/caddy-security@latest \
    --with github.com/infogulch/xtemplate-caddy \
    --with github.com/WingLim/caddy-webhook
FROM caddy:alpine

COPY --from=builder /usr/bin/caddy /usr/bin/caddy