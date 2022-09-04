### Git create repo

1. Создаем папку, проект: `mkdir myproject`
2. Открываем папку: `cd myproject`
3. Инициализируем `git init`
4. Добавляем все файлы в индекс: `git add .`
5. Делаем коммит: `git commit -m "Init project"
6. Указываем репозиторий куда выливать будем: HTTP - `git remote add origin https://github.com/USERNAME/MYPROJECT.git`
   SSH - `git remote add origin git@github.com:USERNAME/MYPROJECT.git`
7. Отправить изменения на удаленный репозиторий `git push -u origin master`

[Подробнее](https://pingvinus.ru/git/1592)

### Изменить git(login-pass) на git(ssh)

1. Получить ссылку на проект `git remote -v`
2. Удалить ссылку на проект `git remote NAME`
3. Добавить новую ссылку на проект - ssh `git remote add NAME URL`

[Подробнее](https://www.atlassian.com/ru/git/tutorials/syncing)

[Некороткий мануал по SSH + GitHub & BitBucket (на Win, почти тоже и на Lin)](https://qna.habr.com/q/231161)

[Подробная настройка под Windows](https://only-to-top.ru/blog/tools/2019-12-08-git-ssh-windows.html)

### Перенести данные в другой репозиторий

|Переменная|значение|
|:---|:---|
|LINK|git@github.com:odi1n/Commands.git|
|BRANCHES_NAME|maset develop project|

1. Добавить новый репозиторий в проект: `git remote add origin LINK`
2. Запушить данные в новый репозиторий `git push -u origin BRANCHES_NAME`
    - пример `git push -u origin master`

#### Включить по умолчани

`git config merge.ff false`

#### Включить для ветки

`git config branch.master.NAME '--no-ff'`

### Удалить git init

`rm -r .git`