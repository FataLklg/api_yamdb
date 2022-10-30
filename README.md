### Описание проекта:

Проект API_YamDB.

Cобирает отзывы (Review) пользователей на произведения (Titles). Произведения делятся на категории: «Книги», «Фильмы», «Музыка». Список категорий (Category) может быть расширен администратором.

*Проект написан на Python 3.7.9*

*Запросы к API начинаются с* `/api/v1`

---

### Как запустить проект:

- ***Клонируйте репозиторий и перейдите в него в командной строке:***

```
git clone https://github.com/FataLklg/api_yamdb.git
```

```
cd api_yamdb
```

- ***Cоздайте и активируйте виртуальное окружение:***

```
python -m venv venv
```

```
source venv/Scripts/activate
```

- ***Обновите модуль pip и установите зависимости из файла requirements.txt:***

```
python -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```
- ***Создайте файл ".env" и пропишите в нём секретный ключ:***

```
touch .env
```
```
SECRET_KEY=<ваш секретный ключ>  # шаблон наполнения .env файла
```
- ***Перейдите в дирректорию api_yamdb:***

```
cd api_yamdb
```
- ***Создайте и примените миграции:***

```
python manage.py makemigrations
python manage.py migrate
```

- ***Запустите проект:***

```
python manage.py runserver
```

---
### Список доступных адресов:

#### - Модуль AUTH:

Аутентификация пользователей реализована на основе JWT-токенов.

Регистрация нового пользователя POST `/auth/signup/`

Получение JWT-токена в обмен на username и confirmation code POST `/auth/token/`

#### - Модуль USERS:
Получение списка всех пользователей GET `/users/`

Добавление пользователя POST `/users/`

Получение пользователя по username GET `/users/{username}/`

Преобразование данных пользователя по username PATCH `/users/{username}/`

Удаление пользователя по username DELETE `/users/{username}/`

Получение данных своей учетной записи GET `/users/me/`

Преобразование данных своей учетной записи PATCH `/users/me/`

#### - Модуль CATEGORIES:
Получение списка всех категорий GET `/categories/`

Добавление новой категории POST `/categories/`

Удаление категории DELETE `/categories/{slug}/`

#### - Модуль GENRE:
Получение списка всех жанров GET `/genres/`

Добавление жанра POST `/genres/`

Удаление жанра DELETE `/genres/{slug}/`

#### - Модуль TITLES:
Получение списка всех произведений GET `/titles/`

Добавление произведения POST `/titles/`

Получение информации о произведении GET `/titles/{titles_id}/`

Частичное обновление информации о произведении PATCH `/titles/{titles_id}/`

Удаление произведения DELETE `/titles/{titles_id}/`

#### - Модуль REVIEWS:
Получение списка всех отзывов GET `/titles/{titles_id}/reviews/`

Добавление нового отзыва POST `/titles/{titles_id}/reviews/`

Получение отзыва по id GET `/titles/{titles_id}/reviews/{review_id}/`

Частичное обновление отзыва по id PATCH `/titles/{titles_id}/reviews/{review_id}/`

Удаление отзыва по id DELETE `/titles/{titles_id}/reviews/{review_id}/`

#### - Модуль COMMENTS:
Получение списка всех комментариев к отзыву GET `/titles/{titles_id}/reviews/{review_id}/comments/`

Добавление комментария к отзыву POST `/titles/{titles_id}/reviews/{review_id}/comments/`

Получение комментария к отзыву GET `/titles/{titles_id}/reviews/{review_id}/comments/{comment_id}/`

Частичное обновление комментария к отзыву PATCH `/titles/{titles_id}/reviews/{review_id}/comments/{comment_id}/`

Удаление комментария к отзыву DELETE `/titles/{titles_id}/reviews/{review_id}/comments/{comment_id}/`

---

### Авторы:

- ##### __Антон Жирков__
- ##### __Виктор Круглый__
- ##### __Антон Тарасов__
