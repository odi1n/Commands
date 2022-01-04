## Docker
### Вытащить файл с Docker Container
1. Подключение к контейнеру, для просмотра структуры проекта, что бы заполнить пути
```docker
docker exec -t -i <container_name> /bin/bash
```
2. Копируем данные из контейнера:
```docker
docker cp <container_name>:<пусть к проекту> <путь куда копируем на текущем сервере>
```

[Подробный пример](https://qna.habr.com/q/407474)
[Поиск](https://www.google.com/search?q=%D0%B4%D0%BE%D1%81%D1%82%D0%B0%D1%82%D1%8C+%D1%84%D0%B0%D0%B9%D0%BB+%D1%81+docker+%D0%BA%D0%BE%D0%BD%D1%82%D0%B5%D0%B9%D0%BD%D0%B5%D1%80%D0%B0&oq=%D0%B4%D0%BE%D1%81%D1%82%D0%B0%D1%82%D1%8C+%D1%84%D0%B0%D0%B9%D0%BB+%D1%81+%D0%B4%D0%BE%D0%BA%D0%B5%D1%80+%D0%BA%D0%BE%D0%BD%D1%82&aqs=chrome.1.69i57j33i22i29i30.6359j0j7&sourceid=chrome&ie=UTF-8)
[Подробнее](https://rtfm.co.ua/docker-skopirovat-fajl-iz-kontejnera-na-xost-mashinu-i-obratno/)

### Получить Ip Docker
```docker
docker network inspect bridge
```
[Подробнее](https://itsecforu.ru/2021/04/02/%F0%9F%90%B3-%D0%BA%D0%B0%D0%BA-%D1%83%D0%B7%D0%BD%D0%B0%D1%82%D1%8C-ip-%D0%B0%D0%B4%D1%80%D0%B5%D1%81-docker-%D0%BA%D0%BE%D0%BD%D1%82%D0%B5%D0%B9%D0%BD%D0%B5%D1%80%D0%B0/)

### Выполнить команду
```docker
docker exec NAME_CONTAINER python3 -v
```

### Получить статистику по контейнерам
```
docker stats --no-stream
```

### Образы
#### Образы локального хранилища
```docker
docker images ls
```

#### Id образов
```docker
docker images -a
```

#### Удаление образов
```docker
docker rmi IMAGE IMAGE IMAGE
```

### Удаление всех образов
```docker
docker rmi $(docker images -a -q)
```

#### Подвешенные образы
```docker
docker images -f dangling=true
```
#### Удаление подвешенных образов
```docker
docker rmi $(docker images -f dangling=true -q)
```

### Контейнеры
#### Запущенные контейнеры
```docker
docker ps
```

#### Запущенные и остановленные
```docker
docker ps -a
```

```docker
docker ps -aq
```

#### Контейнер докера с размером
```docker
docker ps -s
```

#### Контейнер - использование диска
```docker
docker system df
```


### Остановить контейнер
```docker
docker stop NAME_CONTAINER
```
vs
```docker
docker stop ID_CONTAINER
```

### Удалить контейнер
```docker
docker rm NAME_CONTAINER NAME_CONTAINER
```

### Убить все контейнеры
```docker
docker kill $(docker ps -q)
```

### Удалить контейнер при выходе
```docker
docker run --rm image_name
```

### Остановить и удалить все контейнеры
```docker
docker rm $(docker ps -a -q)
```

### Удалить все образы
```docker
docker rmi $(docker images -q)
```

### Log 
```docker
docker logs -f NAME_CONTAINER
```


## Docker-Compose
### Собрать
```docker
docker-compose build
```

### Выполнить
```docker
docker-compose up
```

### Собрать и выполнить
```docker
docker-compose up -d --build
```

### Запустить
```docker
docker-compose start
```

### Остановить
```docker
docker-compose stop
```

### Интересные команды
[Подробнее](https://devacademy.ru/article/kak-udalit-obrazy-kontieiniery-i-toma-docker)

[Подробнее](https://www.digitalocean.com/community/tutorials/how-to-remove-docker-images-containers-and-volumes-ru)

[Подробнее](https://www.codenotary.com/blog/extremely-useful-docker-commands/)

[Подробнее](https://www.digitalocean.com/community/tutorials/how-to-remove-docker-images-containers-and-volumes-ru)

[Подробнее](https://devacademy.ru/article/kak-udalit-obrazy-kontieiniery-i-toma-docker)


