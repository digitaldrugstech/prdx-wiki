# Локальная разработка вики

Этот гайд для Claude-агента, который помогает редактировать вики.

## Что нужно установить

- **Node.js** (любая LTS версия, например 20 или 22)
- **pnpm** — `npm install -g pnpm`
- **Git**

## Первоначальная установка

### 1. Клонировать два репозитория

```bash
# Репозиторий сайта (фронтенд)
git clone https://github.com/digitaldrugstech/plasmo-rw-frontend

# Репозиторий вики (MDX-контент)
git clone https://github.com/digitaldrugstech/prdx-wiki
```

Положи их рядом, например:
```
~/projects/
├── plasmo-rw-frontend/
└── prdx-wiki/
```

### 2. Установить зависимости фронтенда

```bash
cd plasmo-rw-frontend
pnpm install
```

### 3. Создать файл `.env.local`

В папке `plasmo-rw-frontend` создай файл `.env.local` со следующим содержимым:

```env
ENVIRONMENT=local
API_BASE_URL=https://prdxso.dev/api/v1
NEXT_PUBLIC_AVATARS_BASE_URL=https://prdxso.dev/avatar
NEXT_PUBLIC_SKINS_BASE_URL=https://prdxso.dev/skin
WIKI_LOCAL_PATH=/абсолютный/путь/до/prdx-wiki
```

Замени `/абсолютный/путь/до/prdx-wiki` на реальный путь, например:
- macOS/Linux: `/Users/username/projects/prdx-wiki`
- Windows: `C:\Users\username\projects\prdx-wiki`

### 4. Запустить сайт

```bash
cd plasmo-rw-frontend
pnpm dev
```

Сайт откроется на `http://localhost:3000`.

Вики доступна по адресу `http://localhost:3000/wiki`.

> **Важно:** после изменения `.env.local` нужно перезапускать `pnpm dev`.

---

## Как редактировать вики

Все файлы вики находятся в `prdx-wiki/pages/`.

### Структура папок

```
prdx-wiki/
├── pages/
│   ├── index.mdx                  ← главная страница /wiki
│   ├── 100-getting-started/
│   │   ├── index.mdx              ← страница раздела /wiki/getting-started
│   │   ├── 100-bedrock.mdx        ← /wiki/getting-started/bedrock
│   │   └── 200-mods.mdx
│   ├── 200-rules/
│   │   ├── index.mdx
│   │   └── ...
│   └── ...
└── assets/
    └── screenshot.png             ← картинки
```

**Числовые префиксы** (`100-`, `200-`, ...) определяют порядок пунктов в меню. Сам URL строится без них: папка `100-getting-started` → URL `/wiki/getting-started`.

### Формат файла MDX

Каждый файл начинается с frontmatter:

```mdx
---
title: "Заголовок страницы"
---

Текст страницы в формате Markdown.

## Подзаголовок

Параграф текста...
```

Поле `title` обязательно — оно отображается в меню и заголовке страницы.

### Как видеть изменения

После сохранения файла достаточно **перезагрузить страницу** в браузере. Кеш не используется в локальном режиме.

### Картинки

1. Положи картинку в `prdx-wiki/assets/`
2. Вставь в MDX:

```mdx
![описание картинки](название-файла.png)
```

Путь указывается относительно папки `assets/` — только имя файла.

---

## Публикация изменений

Когда правки готовы — сделай коммит и пуш в `prdx-wiki`:

```bash
cd prdx-wiki
git add .
git commit -m "описание изменений"
git push
```

Сайт на `prdxso.dev` подтянет изменения автоматически в течение часа (кеш GitHub API — 1 час). Чтобы обновить немедленно, суперадмин может нажать кнопку "Обновить вики" на странице вики.

---

## Частые проблемы

**Страница вики показывает "Not found"**
— Проверь, что путь в `WIKI_LOCAL_PATH` правильный и папка `pages/` существует внутри.

**Вики недоступна, редирект на главную**
— Нужно войти в аккаунт на сайте. Вики закрыта для пользователей без специальной роли. Используй кнопку "Войти" — она авторизует через prdxso.dev.

**Картинки не отображаются**
— Убедись что файл лежит в `assets/` (не в подпапке) и имя указано правильно.

**После изменения `.env.local` вики читает с GitHub, а не локально**
— Перезапусти `pnpm dev` (Ctrl+C, затем снова `pnpm dev`).
