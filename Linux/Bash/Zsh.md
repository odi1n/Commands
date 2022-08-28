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