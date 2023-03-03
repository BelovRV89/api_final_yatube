## Описание.

Проект управления записями в БД через API.

Позволяет работать с моделями: 
Post - публикации 
Comment - комментарии 
Group - группы пользователей 
Follow - подписчики

## Установка

Клонировать репозиторию

```
git clone https://github.com/AkobArm/api_final_yatube
```

Перейти в папку 

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение
```
python -m venv env
```

```
. env/bin/activate
```

Обновить Pip

```
pip install --upgrade pip
```

Установить зависимости из файла requirements.txt

```
pip install -r requirements.txt
```

Выполнить миграции

```
python manage.py migrate
```

Запустить проект
```
python manage.py runserver
```

Получение токена
```
http://127.0.0.1:8000/api/v1/jwt/create/

Пример:
```

Получение публикаций
```
http://127.0.0.1:8000/api/v1/posts/

Пример Ответа:
{
  "count": 123,
  "next": "http://api.example.org/accounts/?offset=400&limit=100",
  "previous": "http://api.example.org/accounts/?offset=200&limit=100",
  "results": [
    {
      "id": 0,
      "author": "string",
      "text": "string",
      "pub_date": "2021-10-14T20:41:29.648Z",
      "image": "string",
      "group": 0
    }
  ]
}
```

Получение комментария
```
http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/

Пример Ответа:
{
  "id": 0,
  "author": "string",
  "text": "string",
  "created": "2019-08-24T14:15:22Z",
  "post": 0
}
```

Получение сообществ
```
http://127.0.0.1:8000/api/v1/groups/

Пример Ответа:
[
  {
    "id": 0,
    "title": "string",
    "slug": "string",
    "description": "string"
  }
]
```

Получение подписок
```
http://127.0.0.1:8000/api/v1/follow/

Пример Ответа:
[
  {
    "user": "string",
    "following": "string"
  }
]
```

