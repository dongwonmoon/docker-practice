FROM nginx:1.25.3
# Nginx conf 삭제
RUN rm /etc/nginx/conf.d/default.conf
COPY default.conf /etc/nginx/conf.d
CMD ["nginx", "-g", "daemon off;"]