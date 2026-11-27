
ARG NGINX_CONF=http

# Pin the exact Nginx version and multi-platform digest for traceable Dependabot updates.
FROM nginx:1.31.9-alpine3.24@sha256:fb4658584bd9a916ffb6f6e365f97c25cfdb2923801f551ea08356e695f14ff7

# Update Alpine packages to their latest available security fixes.
RUN apk update && apk upgrade --no-cache

ARG NGINX_CONF
ENV NGINX_PORT=80

COPY "conf.d/${NGINX_CONF}.conf" /etc/nginx/templates/default.conf.template

WORKDIR /var/www/html
