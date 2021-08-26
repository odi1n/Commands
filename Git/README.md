## Git ssh
### Добавление ssh ключа
1. Создать ключ ssh
- [Подробнее](https://git-scm.com/book/en/v2/Git-on-the-Server-Generating-Your-SSH-Public-Key)
- [Подробнее](https://github.community/t/key-is-invalid-you-must-supply-a-key-in-openssh-public-key-format/170135/5)
- [Подробнее Windows](https://stackoverflow.com/questions/10476360/key-is-invalid-message-on-github)
2. Добавить ssh на [github](https://github.com/settings/keys)

### Изменить git(login-pass) на git(ssh)
1. Получить ссылку на проект `git remote -v`
2. Удалить ссылку на проект `git remote NAME`
3. Добавить новую ссылку на проект - ssh `git remote add NAME URL`

[Подробнее](https://www.atlassian.com/ru/git/tutorials/syncing)

[Некороткий мануал по SSH + GitHub & BitBucket (на Win, почти тоже и на Lin)](https://qna.habr.com/q/231161)

[Подробная настройка под Windows](https://only-to-top.ru/blog/tools/2019-12-08-git-ssh-windows.html)

### Git merge --no-ff
#### Включить по умолчани
`git config merge.ff false`

#### Включить для ветки
`git config branch.master.NAME '--no-ff'`


## Другое
### Проверить изменения
`git status`

### Добавить все файлы в коммит
`git add .`

### Сделать коммит
`git commit -m "MESSAGE COMMIT"`

### Сделать коммит и пуш
`git commit -am 'MESSAGE'`

### Изменить сообщение последнего локального коммита
`git commit --amend`

### Изменить сообщение удаленного коммита
```
git reset —soft HEAD~1 – «откатываемся» на один коммит назад
git commit -a -m «commit text» – делаем нужные правки и коммитимся
git push -f origin master – отправляем в удаленный репозиторий
```

### Откатиться к указанному комиту
`git checkout ID_коммита`

[Подробнее](https://open2web.com.ua/blog/kak-vernutsya-otkatitsya-k-bolee-rannemu-kommitu.html)


### Объединение коммитов (с использованием git rebase).
1. Ввести команду:
    - Если коммиты находятся в верху, то есть последние: 
    
    `git rebase -i HEAD~2`, 2 - количество последних коммитов
    - Если коммиты не являются последними, то в команде git rebase -i HEAD~n вместо HEAD необходимо указать хеш коммита (SHA1), а после символа тильда количество коммитов, которое вы хотите объединить
    
    `git rebase -i ae88544~3`
2. В текстовом редакторе везде кроме первой строки заменить `pick` на `s`/`sqush`
3. В текстовом редакторе будет предложенно ввести сообщение к коммиту, который и является объединением двух коммитов:

[Подробнее](https://pingvinus.ru/git/1591)
[Подробнее](https://www.google.com/search?q=git+%D0%BE%D0%B1%D1%8A%D0%B5%D0%B4%D0%B8%D0%BD%D0%B8%D1%82%D1%8C+%D0%BA%D0%BE%D0%BC%D0%BC%D0%B8%D1%82%D1%8B+%D0%B2+%D0%BE%D0%B4%D0%B8%D0%BD&sxsrf=ALeKk00BaphkNl3aL2CkVZodTNL1Ftw7Dw%3A1619593880890&ei=mAqJYILyNayEwPAPxd2mmAo&oq=git+%D0%BE%D0%B1%D1%8A%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D1%82%D1%8C+&gs_lcp=Cgdnd3Mtd2l6EAMYAjIHCCMQsQIQJzIHCCMQsQIQJzIECAAQCjIECAAQCjIECAAQCjoICAAQsQMQgwE6AggAOgQIABADOggILhCxAxCTAjoFCC4QsQM6BQgAELEDOgYIABAKEAE6CQgAELEDEAoQAToECCMQJzoECAAQQzoHCAAQsQMQQ1Dmu54BWLTkngFgxPaeAWgAcAJ4AIAB1AGIAfUOkgEGMTIuNS4xmAEBoAEBqgEHZ3dzLXdpesABAQ&sclient=gws-wiz)

### Удалить локальный коммита
1. Отмена последнего коммита: 
    `git reset HEAD~`
    или
    `git checkout -f`
2. Отмена нескольких коммитов:
    `git reset HEAD~5`
3. Удалить неотслеживаемые файлы:
    `git clean -dxf`


### Удалить удаленный коммит
1. Выбрать: 
    `git reset --hard HEAD~1`

2. Применить изменения:
    `git push --force`

3. Все текущие изнения перенести в новую ветку:
    ` git checkout -b NAME_VETKA`

[Подробнее](https://tproger.ru/translations/most-common-git-screwupsquestions-and-solutions/)
[Подробнее](https://pingvinus.ru/git/1581)



[Подробнее](https://pingvinus.ru/git/1581)


### Отменить локальное изменения
`git reset --hard HEAD`

### Откатить коммит и взять его изменения
`git reset --soft HEAD~1`


### Изменить название ветки
Для переименования ветки, загруженной на удалённый сервер, нужно вначале переименовать ветку локально, а затем выгрузить изменения обратно, удалив предыдущую ветку на сервере.

```
git branch -m старое_название новое_название
git push origin :старое_название новое_название
```
    
Во второй строчке обратите внимание на двоеточие перед старым именем ветки — это команда для удаления ветки на сервере.

### Кол-во коммитов
#### Всего
    `git rev-list --count HEAD`

#### Всего в ветке
    `git rev-list --count <branch-name>`

#### Если вы хотите считать коммиты на ветке, созданные с момента создания ветки
    `git rev-list --count HEAD ^<branch-name>`

#### Не учитывая слияния
    `git rev-list --no-merges --count HEAD ^develop`
    
## Ветки
### Удалить ветку 
- локально
    ```
    git branch --delete <branch>
    git branch -d <branch> # Shorter version
    git branch -D <branch> # Force-delete un-merged branches
    ```
- удаленную ветку
    branch - `api1`(моя ветка)
    ```
    git push origin --delete <branch>  # Git version 1.7.0 or newer
    git push origin -d <branch>        # Shorter version (Git 1.7.0 or newer)
    git push origin :<branch>          # Git versions older than 1.7.0
    ```
[Подробнее](https://coderoad.ru/2003505/%D0%9A%D0%B0%D0%BA-%D1%83%D0%B4%D0%B0%D0%BB%D0%B8%D1%82%D1%8C-%D1%84%D0%B0%D0%B9%D0%BB-Git-branch-%D0%BB%D0%BE%D0%BA%D0%B0%D0%BB%D1%8C%D0%BD%D0%BE-%D0%B8-%D1%83%D0%B4%D0%B0%D0%BB%D0%B5%D0%BD%D0%BD%D0%BE#:~:text=%D0%92%20%D0%BE%D1%82%D0%BB%D0%B8%D1%87%D0%B8%D0%B5%20%D0%BE%D1%82%20%D0%BB%D0%BE%D0%BA%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D1%85%20%D0%B2%D0%B5%D1%82%D0%B2%D0%B5%D0%B9,%D1%81%D0%BB%D1%83%D1%87%D0%B0%D0%B5%20origin%20%D0%BF%D0%BE%D1%81%D0%BB%D0%B5%20git%20push.)

### Получить все ветки
`git branch -a`

### Получить локальные ветки
`git branch`

### Получить только удаленные
`git branch -r`

### Архивация веток
- Для архивации и удаления ветки:

    ```
    git tag archive/<branchname> <branchname>
    git branch -d <branchname>
    ```

- Чтобы восстановить ветку через некоторое время:

    ```git checkout -b <branchname> archive/<branchname>```

### Загружаем локальные теги на удаленный сервер
`git push origin --tags`

[Очень подробно](https://dev.to/clsource/archiving-git-branches-3k70)
[Подробнее](https://qastack.ru/programming/1307114/how-can-i-archive-git-branches),
[Подробнее](https://coderoad.ru/1307114/%D0%9A%D0%B0%D0%BA-%D1%8F-%D0%BC%D0%BE%D0%B3%D1%83-%D0%B0%D1%80%D1%85%D0%B8%D0%B2%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D1%82%D1%8C-git-%D0%B2%D0%B5%D1%82%D0%BA%D0%B8)

## Теги

### Получить все удаленные теги
`git ls-remote --tags`

### Просмотр всех архивированных веток
```
git tag --list
```

### Удалить локальный тег
```
git tag -d release/aug2002
```

### Удалить удаленный тег
```
git tag -d release/aug2002
git push origin :refs/tags/release/aug2002
```

### Изменить название тега
Вот как я переименовываю тег oldв new:

```
git tag new old
git tag -d old
git push origin new :old
```

Двоеточие в команде push удаляет тег из удаленного репозитория. Если вы этого не сделаете, Git создаст старый тег на вашем компьютере, когда вы его потянете. Наконец, убедитесь, что другие пользователи удалили удаленный тег. Скажите им (коллегам) выполнить следующую команду:

```git pull --prune --tags```

Обратите внимание, что при изменении аннотированного тега необходимо убедиться, что новое имя тега ссылается на базовую фиксацию, а не на старый объект аннотированного тега, который вы собираетесь удалить. Поэтому используйте:

```git tag -a new old^{}```

вместо git tag new old(это потому, что аннотированные теги являются объектами, а легкие теги - нет, подробнее в этом ответе ).

[Поподробнее](https://stackoverflow.com/questions/1028649/how-do-you-rename-a-git-tag)
