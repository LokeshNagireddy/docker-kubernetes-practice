FROM almalinux
RUN yum install nginx -y
RUN rm -rf /usr/share/nginx/html/index.html
COPY hi.html /usr/share/nginx/html/
