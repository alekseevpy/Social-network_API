# API для социальной сети

## О проекте

Данный проект - это API [социальной сети](https://github.com/alekseevpy/Yatube).

С помощью API можно запрашивать данные о постах, группах, комментариях и подписках в социальной сети, а также создавать новые и изменять их.

Документацию к API можно найти  по [👉адресу](http://localhost:8000/redoc/) после запуска проекта.

Автор: [Lev Alekseev](https://github.com/alekseevpy)

## Технологии

Python 3.9, Django 3.2, DRF, JWT + Djoser

## Как запустить проект

- Клонировать репозиторий и перейти в него в командной строке:

```bash
git clone https://github.com/alekseevpy/Social-network_API.git
cd api_social_network
```

- Cоздать и активировать виртуальное окружение:

```bash
python3 -m venv env
source venv/Scripts/activate
```

- Установить зависимости из файла requirements.txt:

```bash
python3 -m pip install --upgrade pip
pip install -r requirements.txt
```

- Выполнить миграции:

```bash
python3 manage.py migrate
```

- Запустить проект:

```bash
python3 manage.py runserver
```

## Примеры запросов

### GET запросы

- `api/v1/posts/`
Список всех публикаций.

- `api/v1/posts/{post_id}/`
Пост с id = 'post_id'.

- `/api/v1/posts/{post_id}/comments/`
Все комментарии к определённому посту.

- `api/v1/posts/{post_id}/comments/{id}/`
Определённый комментарий.

- `api/v1/groups/`
Все группы соцю сети.

- `api/v1/groups/{id}`
Определённая группа.

- `api/v1/follow/`
Все подписки пользователя, который запрашивает ресурс.

### POST запросы

- `api/v1/posts/`
Создать новый пост.
- `/api/v1/posts/{post_id}/comments/`
Создать новый комментарий.
- `api/v1/follow/`
Подписаться на автора.

Информацию по другим запросам и примеры их выполнения вы можете найти в подробной документации к API, запустив проект и перейдя по адресу:

```bash
http://localhost:8000/redoc/
```
