FROM haroldli/alist-base:latest

LABEL MAINTAINER="Har01d"

ENV MEM_OPT="-Xmx512M" ALIST_PORT=5344 INSTALL=new

COPY config/alist.json /

COPY scripts/entrypoint.sh /
COPY scripts/init.sh /

COPY data/tvbox.zip /
COPY data/base_version /
COPY data/cat.zip /
COPY data/pg.zip /
COPY data/zx.zip /

COPY target/application/ ./

COPY data/version /app_version

EXPOSE 4567 5244

ENTRYPOINT ["/entrypoint.sh"]

CMD ["81", "--spring.profiles.active=production,docker"]
