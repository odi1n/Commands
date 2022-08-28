### Узнать место занимаемое на диске

```
df -h
```

### Получить ip текущей машины

```
wget -qO- eth0.me
```

### Получить все открытые порты

```
ss -plnut
```

#### Сортировка по порту

```
sudo ss -tulpn | grep :80
```

### Получить все процессы

```
ps aux
```

### Получить выборочно

```
ps aux | grep django
```

### Убить процесс

```
kill -9 28691
```

28691 - номер процесса

### Открыть hosts файл

```
sudo nano /etc/hosts
```

### Удалить папку с файлами

```
rm -rf DIRECTORY_NAME
```

### Получить статус приложения

```
service postgresql status
```

или

```
systemctl status postgresql
```

### Старт приложения

```
service postgresql start
```

или

```
systemctl start postgresql
```

### Рестарт приложения

```
service postgresql restart
```

или

```
systemctl restart postgresql
```

### Стоп приложения

```
service postgresql stop
```

или

```
systemctl stop postgresql
```

### Cоздания ссылок - ярлык

```
ln <original> <link>
```

или же например

```
 ln -s /etc/nginx/sites-available/default /etc/nginx/sites-enabled/
 ```

### Получить лог приложения

 ```
 journalctl -xeu nginx.service
 ```

