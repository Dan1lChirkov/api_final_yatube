# api_final

### API для Yatube:
API для Yatube-проект для блоггеров Yatube.
Тут не только люди, но и блоггеры могут создавать посты, писать комментарии, подписываться друг на друга и многое другое.

### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке, например так:
```
git clone <ссылка с GitHub>
```

```
cd api_final_yatube
```
Cоздать и активировать виртуальное окружение:

```
python -m venv venv
```

```
source venv/Scripts/activate
```

```
python3 -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python manage.py migrate
```

Запустить проект:

```
python manage.py runserver
```
### Некоторые примеры запросов к API:
Получаем список всех постов или создаём новый пост(GET,POST):
```
api/v1/posts/
```
Получаем, редактируем или удаляем пост с идентификатором{post_id}(GET, PUT, PATCH, DELETE):
```
api/v1/posts/{post_id}/
```
Получаем список всех комментариев поста с идентификатором post_id(GET):
```
api/v1/posts/{post_id}/comments/
```
Cоздаём новый комментарий для поста с идентификатором {post_id}(POST):
```
api/v1/posts/{post_id}/comments/
```
Получаем, редактируем или удаляем комментарий с идентификатором {comment_id} в посте с id=post_id(GET, PUT, PATCH, DELETE):
```
api/v1/posts/{post_id}/comments/{comment_id}/
```