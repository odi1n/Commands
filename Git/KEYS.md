# Keys

## Добавление ssh ключа

1. Создать ключ ssh

- [Подробнее](https://git-scm.com/book/en/v2/Git-on-the-Server-Generating-Your-SSH-Public-Key)
- [Подробнее](https://github.community/t/key-is-invalid-you-must-supply-a-key-in-openssh-public-key-format/170135/5)
- [Подробнее Windows](https://stackoverflow.com/questions/10476360/key-is-invalid-message-on-github)

Сгенерировать ключ:

```
ssh-keygen -o
```

Если ключ есть:

```
cd ~/.ssh
ls
cat ~/.ssh/id_rsa.pub
```

2. Добавить ssh на [github](https://github.com/settings/keys)

## Проверить подключение
```
ssh -T git@github.com
```
