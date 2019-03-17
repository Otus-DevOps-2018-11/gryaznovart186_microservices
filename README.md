# gryaznovart186_microservices ![BuildStatus](https://travis-ci.com/Otus-DevOps-2018-11/gryaznovart186_microservices.svg?branch=master)

## ДЗ №12 Технология контейнеризации.Введение в Docker

- Установил Docker, docker-compose, docker-machine
- Запущены Docker контейнеры
- Посмотрел список всех контейнеров ```docker ps -a``` и cписок сохранненных образов ```docker images ```
- Запустил и подключился к старому контейнеру ```docker start <u_container_id> ``` и  ```docker attach <u_container_id> ```
- Запустил BASH в контейнере  ```docker exec -it <u_container_id> bash ```
- Создал image из контейнера ```docker commit <u_container_id> yourname/ubuntu-tmp-file```
- Сохранил вывод команды ```docker images``` в файл docker-1.log
