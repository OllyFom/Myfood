# Foodgram — «Продуктовый помощник»

## Описание проекта

Foodgram — это современное веб-приложение для любителей кулинарии, которое позволяет:
- 📝 Создавать и публиковать собственные рецепты
- ❤️ Добавлять понравившиеся рецепты в избранное
- 👥 Подписываться на любимых авторов
- 🛒 Формировать список покупок для выбранных рецептов
- 🔍 Искать рецепты по ингредиентам и тегам

Проект разработан в рамках обучения в Яндекс.Практикуме и включает:
- Мощный backend на Django REST Framework
- Удобный фронтенд на React
- Полноценное REST API
- Систему аутентификации через токены

## Технологии

![Python](https://img.shields.io/badge/Python-3.9-blue)
![Django](https://img.shields.io/badge/Django-3.2-green)
![DRF](https://img.shields.io/badge/Django_REST_Framework-3.12-red)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-13-blue)
![Docker](https://img.shields.io/badge/Docker-20.10-cyan)
![Nginx](https://img.shields.io/badge/Nginx-1.21-brightgreen)

## Быстрый старт

### Требования
- Docker 20.10+
- Docker Compose 1.29+

### Установка
1. Клонируйте репозиторий:
```bash
git clone https://github.com/OllyFom/Myfood.git
cd foodgram
```

2. Создайте файл `.env` в корневой директории (пример настроек в `.env.example`)

3. Запустите проект:
```bash
docker-compose up -d --build
```

4. Примените миграции:
```bash
docker-compose exec backend python manage.py migrate
```

5. Создайте суперпользователя:
```bash
docker-compose exec backend python manage.py createsuperuser
```

6. Соберите статику:
```bash
docker-compose exec backend python manage.py collectstatic --no-input
```

После выполнения этих шагов проект будет доступен по адресу `http://localhost/`

## Документация API

Полная документация API доступна после запуска проекта по адресу:
`http://localhost/api/docs/`

Основные эндпоинты:
- `POST /api/users/` — регистрация нового пользователя
- `POST /api/auth/token/login/` — получение токена авторизации
- `GET /api/recipes/` — список всех рецептов
- `POST /api/recipes/{id}/favorite/` — добавить рецепт в избранное
- `GET /api/users/subscriptions/` — список подписок
- `GET /api/recipes/download_shopping_cart/` — скачать список покупок

## Особенности реализации

### Backend
- Кастомная система прав доступа
- Оптимизированные запросы к БД
- Пагинация и фильтрация
- Валидация данных
- Система тегов для рецептов

### Frontend
- Адаптивный интерфейс
- Удобные формы создания/редактирования
- Интерактивные элементы
- Система уведомлений

### Инфраструктура
- Контейнеризация приложения
- Автоматическое развертывание (CI/CD)
- Надежная система резервного копирования
- Мониторинг ошибок

## Лицензия

MIT License. Подробнее см. в файле LICENSE.

## Доступ

- **Сайт**: [https://netkann.ru](https://netkann.ru)  

---
## Автор
Фомина Ольга А-07-22
