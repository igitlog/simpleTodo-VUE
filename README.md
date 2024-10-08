# Todo приложение на Vue 3 + TypeScript

Это простое Todo приложение, разработанное с использованием Vue 3 и TypeScript. Оно позволяет пользователям добавлять и удалять задачи из списка.

## Функциональность

- Добавление новых задач
- Отображение списка задач
- Удаление задач из списка

## Технологии

- Vue 3
- TypeScript
- Vite (для сборки и разработки)

## Структура проекта
project-root/
│
├── public/
│ └── index.html
│
├── src/
│ ├── components/
│ │ └── TodoItem.vue
│ ├── App.vue
│ ├── main.ts
│ ├── style.css
│ └── types.ts
│
├── .gitignore
├── package.json
├── README.md
├── tsconfig.json
└── vite.config.ts


## Установка и запуск

1. Клонируйте репозиторий:
   ```
   git clone [URL вашего репозитория]
   ```

2. Перейдите в директорию проекта:
   ```
   cd [имя директории проекта]
   ```

3. Установите зависимости:
   ```
   npm install
   ```

4. Запустите проект в режиме разработки:
   ```
   npm run dev
   ```

5. Откройте браузер и перейдите по адресу `http://localhost:5173`

## Сборка для продакшена

Для создания продакшен-версии выполните:

npm run build


Собранные файлы будут находиться в директории `dist/`.

## Компоненты

### App.vue

Основной компонент приложения. Содержит логику для управления списком задач и отображает компоненты `TodoItem`.

### TodoItem.vue

Компонент для отображения отдельной задачи. Принимает текст задачи и обрабатывает событие удаления.

## Типы

В файле `src/types.ts` определен интерфейс `Todo`:

## Стилизация

Стили определены в файле `src/style.css`. Приложение использует современный, минималистичный дизайн с темной цветовой схемой.

## Дальнейшее развитие

Возможные улучшения проекта:

- Добавление возможности редактирования задач
- Реализация сохранения задач в локальном хранилище или на сервере
- Добавление категорий или тегов для задач
- Реализация функции поиска по задачам
- Добавление возможности установки приоритетов для задач

## Лицензия

[MIT]