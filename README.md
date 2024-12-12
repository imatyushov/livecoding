# Livecoding


Livecoding - это полнофункциональное веб-приложение, аналог PasteBin, позволяющее пользователям сохранять любой код до 10МБ без регистрации. Приложение также предоставляет открытое API и использует редактор Monaco Editor (аналог Visual Studio Code).
Особенности

- Сохранение кода: Пользователи могут сохранять любой код до 10МБ.
- Без регистрации: Не требуется регистрация для использования сервиса.
- Monaco Editor: Встроенный редактор кода, аналогичный Visual Studio Code.
- Открытое API: API для взаимодействия с приложением.

## Будущие варианты

- Добавление сокетов для редактирования несколькими пользователями: Возможность совместного редактирования кода в реальном времени. ⌛
- Файловая архитектура: Поддержка работы с файлами и директориями, что позволит пользователям организовывать свои проекты более эффективно. ❌
- Маштабируемая БД: Перевод хранения кода с PostgreSQL на S3  
  
## Технологии

- Backend: NestJS (TypeScript)
- Frontend: VueJS (TypeScript)
- SSR: Nuxt
- DB: PostgeSQL, S3, Redis
- Broker: Apache Kafka

## Особенности

- **Сохранение кода**: Пользователи могут сохранять любой код до 10МБ.
- **Без регистрации**: Не требуется регистрация для использования сервиса.
- **Monaco Editor**: Встроенный редактор кода, аналогичный Visual Studio Code.
- **Открытое API**: API для взаимодействия с приложением.

## Запуск и установка

### Предварительные требования

Убедитесь, что у вас установлены следующие программы:

- Node.js (рекомендуется версия LTS)
- Yarn

### Клонирование репозитория

```bash
git clone https://github.com/yourusername/codether.git
cd codether
```
Установка зависимостей

```bash
cd frontend
yarn install
cd ../backend
yarn install
```
### Запуск Backend сервера

Перейдите в директорию server и запустите сервер:

```bash
cd backend
yarn start
```

### Запуск Frontend сервера

Перейдите в директорию client и запустите сервер:

```bash
cd frontend
yarn serve
```
Приложение будет доступно по адресу http://localhost:8080.
Открытое API

## API предоставляет следующие эндпоинты:
### Подробнее в swagger по /docs
    
    POST /api/code/create - Сохранить новый код.
    POST /api/code/get/:shortid - Получить сохраненный код по ID.
    POST /api/code/update/:shortid - Обновление кода

### Пример запроса

```bash
curl -X POST http://localhost:3000/api/code/create -H "Content-Type: application/json" -d '{"code": "console.log(\"Hello World\");"}'
```
Структура проекта

bash

    codether/
    ├── frontend/          # VueJS frontend
    │   ├── src/
    │   ├── public/
    │   └── ...
    ├── backend/          # NestJS backend
    │   ├── src/
    │   ├── test/
    │   └── ...
    ├── README.md
    └── package.json


