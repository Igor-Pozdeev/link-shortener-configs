# На базе какого образа будет собран наш образ
FROM amazoncorretto:17.0.1-alpine
# Команда копирует jar из директории проекта в корневую папку образа
COPY ./link-shortener*.jar ./link-shortener.jar
COPY application-release.yaml ./application-release.yaml
# Чтобы время в контейнере не отличалось от времени локальной машины
ENV TZ=Europe/Moscow
# Информирует: какой порт будет открыт. Никак не влияет на поведение контейнера
EXPOSE 8080
# Запускает описанную команду при старте контейнера
CMD ["java", "-jar", "./link-shortener.jar"]
