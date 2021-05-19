### Запустить сервер
`python manage.py runserver`

### Применить изменения модели
`python manage.py makemigrations`

### Сделать миграцию
`python manage.py migrate`

### Собрать статические файлы
`python manage.py colectstatic`

### Venv(Виртуальное окружение)
1. Установка
  - Linux
  
    `sudo apt-get install python3-venv`
    
2. Создание
  - Windows
  
    `python -m venv venv`
  - Linux
  
    `python3 -m venv venv`

3. Активация
  - Windows
  
    `.\venv\Scripts\activate`
  - Linux
  
    `source venv/bin/activate`

### Debuging
`python manage.py shell`

Перейти к нужной моделе
```python
from blogs.models import News

News(title="hi", content="Hellow World")
news = _ # Получить значение предыдущего запроса
news.save()
```

### Выполнить тесты
`python manage.py test`

### Посмотреть Sql Запрос

`python manage.py sqlmigrate NAME_PROJECT NUMBER_MIGRATE`

Пример:
`python manage.py sqlmigrate news 0001`
