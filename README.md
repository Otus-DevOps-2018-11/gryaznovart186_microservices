# gryaznovart186_microservices ![BuildStatus](https://travis-ci.com/Otus-DevOps-2018-11/gryaznovart186_microservices.svg?branch=master)

## ДЗ №14 Технология контейнеризации.Введение в Docker

- Установил Docker, docker-compose, docker-machine
- Запущены Docker контейнеры
- Посмотрел список всех контейнеров ```docker ps -a``` и cписок сохранненных образов ```docker images ```
- Запустил и подключился к старому контейнеру ```docker start <u_container_id> ``` и  ```docker attach <u_container_id> ```
- Запустил BASH в контейнере  ```docker exec -it <u_container_id> bash ```
- Создал image из контейнера ```docker commit <u_container_id> yourname/ubuntu-tmp-file```
- Сохранил вывод команды ```docker images``` в файл docker-1.log

## ДЗ №16 Docker-образы Микросервисы

Запуск контейнеров с прокидванием переменных окружения

# gryaznovart186_microservices ![BuildStatus](https://travis-ci.com/Otus-DevOps-2018-11/gryaznovart186_microservices.svg?branch=master)

## ДЗ №14 Технология контейнеризации.Введение в Docker

- Установил Docker, docker-compose, docker-machine
- Запущены Docker контейнеры
- Посмотрел список всех контейнеров ```docker ps -a``` и cписок сохранненных образов ```docker images ```
- Запустил и подключился к старому контейнеру ```docker start <u_container_id> ``` и  ```docker attach <u_container_id> ```
- Запустил BASH в контейнере  ```docker exec -it <u_container_id> bash ```
- Создал image из контейнера ```docker commit <u_container_id> yourname/ubuntu-tmp-file```
- Сохранил вывод команды ```docker images``` в файл docker-1.log

## ДЗ №16 Docker-образы Микросервисы

Запуск контейнеров с прокидванием переменных окружения

`docker run --name post_db -d --network=reddit --network-alias=post_db_env --network-alias=comment_db_env -v reddit_db:/data/db mongo:latest`

`docker run --name post -d --network=reddit --network-alias=post_env -e POST_DATABASE_HOST=post_db_env gryaznovart186/post:1.0`

`docker run --name comment -d --network=reddit --network-alias=comment_env -e COMMENT_DATABASE_HOST=comment_db_env gryaznovart186/comment:2.0`

`docker run --name ui -d --network=reddit -p 9292:9292 -e POST_SERVICE_HOST=post_env -e COMMENT_SERVICE_HOST=comment_env gryaznovart186/ui:2.1`

## ДЗ №17 Docker: сети, docker-compose
Базовое имя проекта, по умолчанию, образуется из имени директории в которой производится запуск
Способы изменения:
 - запустить docker-compose up -d -p new_project_name
 - задать в переменной окружения COMPOSE_PROJECT_NAME

## ДЗ №19 Устройство Gitlab CI
 - С помощью docker-mahine подготовлена VM для gitlab
 - С помощью docker-copmpose запущен docker с gitlab
 - Создан проект  и пр.
 - С помощью docker-copmpose запущен docker с gitlab runner, runner подключен к gitlab
 - Подготовлен pipeline c различными окружениями


## ДЗ №20 Введение вмониторинг. Системы мониторинга.
Ссылки на образы:
 - https://cloud.docker.com/repository/docker/gryaznovart186/prometheus
 - https://cloud.docker.com/repository/docker/gryaznovart186/post
 - https://cloud.docker.com/repository/docker/gryaznovart186/comment
 - https://cloud.docker.com/repository/docker/gryaznovart186/ui

## ДЗ №21 Мониторингприложения иинфраструктуры
Ссылки на образы:
 - https://cloud.docker.com/repository/docker/gryaznovart186/prometheus
 - https://cloud.docker.com/repository/docker/gryaznovart186/post
 - https://cloud.docker.com/repository/docker/gryaznovart186/comment
 - https://cloud.docker.com/repository/docker/gryaznovart186/ui
 - https://cloud.docker.com/repository/docker/gryaznovart186/alertmanager
