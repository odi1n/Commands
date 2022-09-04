# SMTP

## Нужно

1. Аккаут в Google
2. Привязать подтверждение авторизации через телефон.
    1. Управление аккаунтом Google
    2. Безопасность
    3. Двухэтапная аутентификация
3. Сделать приложение в кабинете
    1. Управление аккаунтом Google
    2. Безопасность
    3. Пароли приложений
    4. Настройки приложения:
        1. Приложение
        2. Устройство
    5. Добавить
    6. Использовать этот пароль

## Conf

```pycon
EMAIL_HOST=smtp.gmail.com
EMAIL_HOST_USER=example@gmail.com
EMAIL_HOST_PASSWORD=password
EMAIL_PORT=587
EMAIL_USE_SSL=False
EMAIL_USE_TLS=True
```