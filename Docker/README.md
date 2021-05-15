### Запустить [postres](./docker-composer/postgres.yml)
1. Скопировать в папку файл postgres.yml
2. Изменить название на docker-composer
3. Выполнить
    ```docker
    docker-composer up --build
    ```
   
### Получить Ip Docker
Здесь вместо идентификатора я буду использовать имя, bridge
```docker
docker network inspect bridge
```
[Подробнее](https://itsecforu.ru/2021/04/02/%F0%9F%90%B3-%D0%BA%D0%B0%D0%BA-%D1%83%D0%B7%D0%BD%D0%B0%D1%82%D1%8C-ip-%D0%B0%D0%B4%D1%80%D0%B5%D1%81-docker-%D0%BA%D0%BE%D0%BD%D1%82%D0%B5%D0%B9%D0%BD%D0%B5%D1%80%D0%B0/)