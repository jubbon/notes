# Docker

![Статус сборки](http://img.shields.io/travis/dotcloud/docker.svg?style=flat)  

[Домашняя страница](http://docker.io)  
[Исходный код](https://github.com/dotcloud/docker)  
[Репозиторий Docker-контейнеров](https://index.docker.io)

Команды
-------


```sh
# Вывести список работающих контейнеров
docker ps
```

```sh
# Вывести список всех контейнеров
docker ps -a
```

Как сделать проброс портов?
---------------------------
```sh
docker run -d -p 22181:2181 <user>/<image> <command> <args>
docker run -d -p 22181:2181 -p 22182:2182 -p 22183:2183 <user>/<image> <command> <args>
```
 - порты 22181, 22182 и 22183 - внешние порты (которые слушает хост)
 - порты 2181, 2182 и 2183 - внутренние порты (которые слушает демон внутри контейнера)

