# Yatube API
### Описание:
***Yatube API*** - сервис позволяющий Вам создавать и просматривать публикации.
С его помощью вы легко загрузите на сайт любимое фото, поделитесь своими мыслями.
Вы можете подписаться на друга или интересного автора и оставить комментарий под его публикацией.


### Как запустить проект:

1. Клонировать репозиторий и перейти в него в командной строке:

```
git clone git@github.com:Aleksandr27041986/api_final_yatube.git
```

```
cd api_final_yatube
```

2. Cоздать и активировать виртуальное окружение:

```
python -m venv env
```

```
source venv/script/activate
```

```
python -m pip install --upgrade pip
```

3. Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

4. Выполнить миграции:

```
python3 manage.py migrate
```

5. Запустить проект:

```
python3 manage.py runserver
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