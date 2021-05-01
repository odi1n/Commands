### Добавить все файлы в коммит
`git add .`

### Сделать коммит
`git commit -m "MESSAGE COMMIT"`

### Объединение коммитов (с использованием git rebase).
1. Ввести команду:
    - Если коммиты находятся в верху, то есть последние: 
    
    `git rebase -i HEAD~2`, 2 - количество последних коммитов
    - Если коммиты не являются последними, то в команде git rebase -i HEAD~n вместо HEAD необходимо указать хеш коммита (SHA1), а после символа тильда количество коммитов, которое вы хотите объединить
    
    `git rebase -i ae88544~3`
2. В текстовом редакторе везде кроме первой строки заменить `pick` на `s`/`sqush`
3. В текстовом редакторе будет предложенно ввести сообщение к коммиту, который и является объединением двух коммитов:

[Подробнее](https://pingvinus.ru/git/1591)

### Склеить коммиты
1. 
[Подробнее](https://www.google.com/search?q=git+%D0%BE%D0%B1%D1%8A%D0%B5%D0%B4%D0%B8%D0%BD%D0%B8%D1%82%D1%8C+%D0%BA%D0%BE%D0%BC%D0%BC%D0%B8%D1%82%D1%8B+%D0%B2+%D0%BE%D0%B4%D0%B8%D0%BD&sxsrf=ALeKk00BaphkNl3aL2CkVZodTNL1Ftw7Dw%3A1619593880890&ei=mAqJYILyNayEwPAPxd2mmAo&oq=git+%D0%BE%D0%B1%D1%8A%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D1%82%D1%8C+&gs_lcp=Cgdnd3Mtd2l6EAMYAjIHCCMQsQIQJzIHCCMQsQIQJzIECAAQCjIECAAQCjIECAAQCjoICAAQsQMQgwE6AggAOgQIABADOggILhCxAxCTAjoFCC4QsQM6BQgAELEDOgYIABAKEAE6CQgAELEDEAoQAToECCMQJzoECAAQQzoHCAAQsQMQQ1Dmu54BWLTkngFgxPaeAWgAcAJ4AIAB1AGIAfUOkgEGMTIuNS4xmAEBoAEBqgEHZ3dzLXdpesABAQ&sclient=gws-wiz)


### Удалить последний коммит
1. Выбрать: 
    `git reset --hard HEAD~1`

2. Применить изменения:
    `git push --force`

3. Все текущие изнения перенести в новую ветку:
    ` git checkout -b NAME_VETKA`

[Подробнее](https://tproger.ru/translations/most-common-git-screwupsquestions-and-solutions/)


### Отмена коммита
1. Отмена последнего коммита: `git reset HEAD~`
2. Отмена нескольких коммитов: `git reset HEAD~`

[Подробнее](https://pingvinus.ru/git/1581)


### Полное удаление последнего коммита
1. Если вы хотите полностью удалить последний коммит, включая все изменения файлов данного коммита, то используется команда:

` git reset --hard HEAD~1`

[Подробнее](https://pingvinus.ru/git/1581)