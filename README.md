# Домашнее задание к занятию 4 «Оркестрация группой Docker контейнеров на примере Docker Compose»

Задание: https://github.com/netology-code/virtd-homeworks/blob/shvirtd-1/05-virt-03-docker-intro/README.md

Все команды выполнялись на ВМ в Yandex Cloud (Ubuntu).

---

## Задача 1

Установлены Docker Engine 29.9.3 и Docker Compose plugin v5.7.0 (Ubuntu 24.04). Docker Hub из облака доступен, зеркала в `daemon.json` не понадобились.

Ссылка на репозиторий: https://hub.docker.com/repository/docker/rostorguev/custom-nginx/general
(публичная страница: https://hub.docker.com/r/rostorguev/custom-nginx)

Файлы: [task1/Dockerfile](task1/Dockerfile), [task1/index.html](task1/index.html)

```dockerfile
FROM nginx:1.29.0
COPY index.html /usr/share/nginx/html/index.html
```

Команды:

```bash
docker pull nginx:1.29.0
docker build -t custom-nginx:1.0.0 .
docker tag custom-nginx:1.0.0 rostorguev/custom-nginx:1.0.0
docker push rostorguev/custom-nginx:1.0.0
```

При `push` слои базового образа помечены `Mounted from library/nginx`: они уже есть на Docker Hub, поэтому загружается только новый слой с `index.html` и служебные данные образа.

---

## Задача 2

_В работе._

---

## Задача 3

_В работе._

---

## Задача 4

_В работе._

---

## Задача 5

_В работе._
