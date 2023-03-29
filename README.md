# Описание

REST API для проекта Yatube - социальной сети для чтения и публикации постов, комментариев к ним.

API доступен только аутентифицированным пользователям. В проекте аутентификация осуществляется по токену TokenAuthentication (Аутентификация по JWT-токену).

Аутентифицированным пользователям разрешено изменение и удаление своего контента; в остальных случаях доступ предоставляется только для чтения.

Работает со всеми модулями социальной сети Yatube: постами, комментариями, группами, подписчиками

Поддерживает методы GET, POST, PUT, PATCH, DELETE

Предоставляет данные в формате JSON

Полная документация (redoc.yaml) доступна по адресу http://localhost:8000/redoc/

# Системные требования
- Python 3.7+
- Works on Linux, Windows, macOS

# Стек технологий:
- Python 3.7
- Django 2.2.16
- Django RESTFramework
- Simple-JWT

# Установка

Клонировать репозиторий и перейти в него в командной строке:

```
https://github.com/Ekaterishe4ka/api_final_yatube.git
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
```

Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```
Ваш проект запустился на http://127.0.0.1:8000/

# Примеры запросов

```
api/v1/posts/ - Получение публикаций
```

```
api/v1/posts/ - Список сообществ
```

```
api/v1/posts/{post_id}/comments/ - Комментарии к публикации
```

```
api/v1/follow/ - Подписки пользователя (доступен только аутентифицированным пользователям)
```

```
api/v1/jwt/create/ - Получение JWT-токена
```

```
api/v1/jwt/refresh/ - Обновление JWT-токена
```

```
api/v1/jwt/verify/ - Проверка JWT-токена
```
