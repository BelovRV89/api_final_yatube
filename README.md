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
```

Получение публикаций
```
http://127.0.0.1:8000/api/v1/posts/
```
