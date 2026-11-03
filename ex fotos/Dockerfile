FROM nginx:alpine

RUN printf 'server {\nlisten 10000;\nserver_name _;\n\nlocation / {\n    root /usr/share/nginx/html;\n    index index.html;\n    try_files $uri $uri/ /index.html;\n}\n}\n' > /etc/nginx/conf.d/default.conf

COPY index.html /usr/share/nginx/html/
COPY *.jpg /usr/share/nginx/html/
COPY *.png /usr/share/nginx/html/

EXPOSE 10000

CMD ["nginx", "-g", "daemon off;"]
