# PHP Frameworks Lab

Лабораторна робота з основ роботи з PHP фреймворками Symfony та Laravel.

**Студент:** Дзядзін Марина Василівна
**Група:** ІПЗ-24-2
**Варіант:** Log  
**Репозиторій:** https://github.com/ipz242dmv-alt/frameworks

## Структура

- `symfony/` — проєкт на Symfony 8.1 (тема: **Log**)
- `laravel/` — проєкт на Laravel 13 (тема: **Log**)

## Модель даних Log

| Поле | Тип | Обов'язкове | Опис |
|------|-----|-------------|------|
| id | string | авто | Унікальний ідентифікатор |
| level | string | ✅ | Рівень: DEBUG, INFO, WARNING, ERROR, CRITICAL |
| message | string | ✅ | Текст повідомлення |
| source | string | ✅ | Джерело події |
| context | array | ❌ | Додаткові дані |
| created_at | string | авто | Дата створення |
| updated_at | string | авто | Дата оновлення |

## CRUD операції

| Метод | Symfony | Laravel | Дія |
|-------|---------|---------|-----|
| GET | /logs | /api/logs | Список усіх логів |
| POST | /logs | /api/logs | Створити лог |
| GET | /logs/{id} | /api/logs/{id} | Отримати за ID |
| PATCH | /logs/{id} | /api/logs/{id} | Оновити лог |
| DELETE | /logs/{id} | /api/logs/{id} | Видалити лог |

## Запуск

```bash
# Symfony
cd symfony && php -S localhost:8000 -t public

# Laravel
cd laravel && php artisan serve --port=8001
```