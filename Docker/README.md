## Docker
### Запустить [postres](docker-compose/postgres/docker-compose.yml)
1. Скопировать в папку файл postgres.yml
2. Выполнить
    ```docker
    docker-composer up --build
    ```
   
### Получить Ip Docker
```docker
docker network inspect bridge
```
[Подробнее](https://itsecforu.ru/2021/04/02/%F0%9F%90%B3-%D0%BA%D0%B0%D0%BA-%D1%83%D0%B7%D0%BD%D0%B0%D1%82%D1%8C-ip-%D0%B0%D0%B4%D1%80%D0%B5%D1%81-docker-%D0%BA%D0%BE%D0%BD%D1%82%D0%B5%D0%B9%D0%BD%D0%B5%D1%80%D0%B0/)

### Выполнить команду
```docker
docker exec NAME_CONTAINER python3 -v
```


### Образы
#### Образы локального хранилища
```docker
docker images ls
```

#### Удаление образов
```docker
docker rmi myimage
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

### Удалить контейнер
```docker
docker rm NAME_CONTAINER
```

### Убить все контейнеры
```docker
docker kill $(docker ps -q)
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
[Подробнее](https://www.codenotary.com/blog/extremely-useful-docker-commands/)

[Подробнее](https://www.digitalocean.com/community/tutorials/how-to-remove-docker-images-containers-and-volumes-ru)

[Подробнее](https://devacademy.ru/article/kak-udalit-obrazy-kontieiniery-i-toma-docker)


