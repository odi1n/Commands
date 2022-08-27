### Узнать место занимаемое на диске
`df -h`

### Получить ip текущей машины
```
wget -qO- eth0.me
```

### Получить все открытые порты 
```ss -plnut```
#### Сортировка по порту
```sudo ss -tulpn | grep :80```

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

## Настройки Bash
### ZSH
#### Версия zsh
```bash
zsh --version
```
#### Установка zsh
```bash
sudo apt install zsh
```
[Подробнее](https://losst.ru/nastrojka-zsh-i-oh-my-zsh)
[Подробнее](http://members.wolfram.com/meng/pages/computing/installing_and_configuring/installing_and_configuring_zsh/#.YXkjI5ozZhG)
[Подробнее](https://www.youtube.com/watch?v=HgI_DJEX0rk)
[Фишки, как пользоваться](https://www.youtube.com/watch?v=f3WUVtcR8YE)
[Подробнее]()

#### Удалить zsh
```bash
sudo apt-get --purge remove zsh
```
или
```bash
chsh -s /bin/bash
```
[Подробнее](https://ubuntugeeks.com/questions/156577/remove-zsh-from-ubuntu-16-04)

#### Изменить настройки zsh
```
nano ~/.zshrc
```

#### Изменить default shell
```bash
chsh -s /bin/bash
```
или
```bash
chsh -s $(which zsh)
```
И перезайти в систему

### Oz my zsh
#### Установка oh my zsh
```bash 
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

#### Удалить oh-my-zsh
```bash
rm .oh-my-zsh/
```

#### Установить плагины
1. [Инструкция как установить](https://youtu.be/ZNHkS4EnXhQ)
2. [Настройка, описание .zshrc](https://dev-props.com/notes/zsh/)
5. [Плагины, настройка](https://losst.ru/nastrojka-zsh-i-oh-my-zsh)
6. [Настройка .zshrc](https://niklan.net/blog/149)
7. [Информация об установке того или иного](https://wiki.rtzra.ru/ubuntu/zsh-oh-my-zsh)


#### Плагины:
1. [Подсвечивает команды](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md)
2. [Авто-дополнение](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md)
3. [Офф плагины](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins)


[Подробнее](https://ohmyz.sh/#install)
[Репо](https://github.com/ohmyzsh/ohmyzsh)
