### Убить процесс
1. Получить все процессы

    `ps aux`
    
2. Убить процесс

    `kill -9 28691`, 28691 - номер процесса
    

### Открыть hosts файл
`sudo nano /etc/hosts`


### Получить статус приложения
`service postgresql status`

### Удалить папку с файлами
`rm -rf DIRECTORY_NAME`

### Старт приложения
`service postgresql start`

### Рестарт приложения
`service postgresql restart`

### Стоп приложения
`service postgresql stop`


## ZSH - Oh My ZSH
### Версия zsh
```bash
zsh --version
```
### Установка zsh
```bash
sudo apt install zsh
```
[Подробнее](https://losst.ru/nastrojka-zsh-i-oh-my-zsh)
[Подробнее](http://members.wolfram.com/meng/pages/computing/installing_and_configuring/installing_and_configuring_zsh/#.YXkjI5ozZhG)
[]()
[]()
[]()

### Удалить zsh
```bash
sudo apt-get --purge remove zsh
```
или
```bash
chsh -s /bin/bash
```
[Подробнее](https://ubuntugeeks.com/questions/156577/remove-zsh-from-ubuntu-16-04)

### Изменить default shell
```bash
chsh -s /bin/bash
```
или
```bash
chsh -s $(which zsh)
```
И перезайти в систему


### Установка oh my zsh
```bash 
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### Удалить oh-my-zsh
```bash
rm .oh-my-zsh/
```

### Установить плагины
1. [Инструкция как установить](https://youtu.be/ZNHkS4EnXhQ)
2. [Подсвечивает команды](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md)
3. [Авто-дополнение](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md)

[Подробнее](https://ohmyz.sh/#install)
[Подроьнее](https://github.com/ohmyzsh/ohmyzsh)
