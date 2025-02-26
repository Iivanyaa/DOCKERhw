FROM nginx:latest

# Копируем статические файлы в контейнер
COPY index.html /usr/share/nginx/html/

#Exposed порт 80 для доступа к HTTP-серверу
EXPOSE 80

# Запуск Nginx
CMD ["nginx", "-g", "daemon off;"]
