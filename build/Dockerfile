FROM --platform=$TARGETPLATFORM dreamacro/clash:v1.18.0

EXPOSE 8080

RUN apk update && apk add nginx

COPY ./dist/ /dashboard
COPY ./build/nginx.conf /etc/nginx
COPY ./build/start.sh /

ENTRYPOINT [ "sh", "/start.sh" ] 