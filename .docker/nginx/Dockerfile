
ARG NGINX_CONF=http

# Pin the exact Nginx version and multi-platform digest for traceable Dependabot updates.
FROM nginx:1.31.6-alpine3.24@sha256:df221db836e1754089190208cee7eeda94f233197056426eda74a43ab1abeac2

# Update Alpine packages to their latest available security fixes.
RUN apk update && apk upgrade --no-cache

ARG NGINX_CONF
ENV NGINX_PORT=80

COPY "conf.d/${NGINX_CONF}.conf" /etc/nginx/templates/default.conf.template

WORKDIR /var/www/html
