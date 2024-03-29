# Yatube API
### Описание:
***Yatube API*** - сервис позволяющий Вам создавать и просматривать публикации.
С его помощью вы легко загрузите на сайт любимое фото, поделитесь своими мыслями.
Вы можете подписаться на друга или интересного автора и оставить комментарий под его публикацией.
***
### Технологии:
Бэкенд представляет собой API написанное с использованием Django Rest Framework, обмен данными идёт с использованием JSON формата. Используется база данных SQLite. Настроена аутентификация по JWT-токену.

### Как запустить проект:

1. Клонировать репозиторий и перейти в него в командной строке:

```bash
git clone git@github.com:Aleksandr27041986/Yatube-api.git
```

```bash
cd Yatube-api
```

2. Cоздать и активировать виртуальное окружение:

```bash
python -m venv venv
```

```bash
source venv/Scripts/activate
```

```bash
python -m pip install --upgrade pip
```

3. Установить зависимости из файла requirements.txt:

```bash
pip install -r requirements.txt
```

4. Выполнить миграции:

```bash
python manage.py migrate
```

5. Запустить проект:

```bash
python manage.py runserver
```

### Примеры запросов:

Адрес для работы с API http://127.0.0.1:8000/api/v1/
Пример Post-запроса по адресу [posts](http://127.0.0.1:8000/api/v1/posts/)
```json
{
"text": "string",
"image": "string",
"group": 0
}
```
Полученный ответ:
```json
{
"id": 0,
"author": "string",
"text": "string",
"pub_date": "2019-08-24T14:15:22Z",
"image": "string",
"group": 0
}
```
Подробнее с примерами запросов и эндпоинтами можно ознакомиться в 
[документации redoc](http://127.0.0.1:8000/redoc/)
