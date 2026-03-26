# prdx-wiki

Вики сервера prdx.so. Контент пишется в MDX (Markdown + JSX компоненты).

## Структура

```
pages/
├── index.mdx                    # Главная вики
├── 100-getting-started/         # Секция "Начать игру"
│   ├── index.mdx
│   └── 100-bedrock.mdx
├── 200-mods/                    # Моды и ресурсы
├── 300-rules/                   # Правила
├── 400-features/                # Механики
├── 500-mko/                     # МКО
└── 600-guides/                  # Гайды
assets/                          # Изображения
```

Нумерация в названиях (`100-`, `200-`) определяет порядок в навигации. Префикс удаляется из URL.

## Frontmatter

Каждый файл начинается с:

```yaml
---
title: "Название страницы"
---
```

## Markdown

Стандартный Markdown + GFM (таблицы, strikethrough). Заголовки `## H2` и `### H3` попадают в оглавление справа.

## Компоненты

### CustomBlock — алерты

Блоки с цветной полоской слева. Типы: `note` (синий), `tip` (зелёный), `important` (фиолетовый), `warn` (оранжевый), `danger` (красный). Без `type` — `note`.

```mdx
<CustomBlock type="note">

#### Заголовок

Текст алерта.

</CustomBlock>
```

### Collapse / CollapseBlock — спойлеры

Раскрывающиеся блоки. `CollapseBlock` группирует несколько, `Collapse` может быть и одиночным.

```mdx
<CollapseBlock>

<Collapse summary="Вопрос?">

Ответ.

</Collapse>

</CollapseBlock>
```

### FatLink — кнопка-ссылка

```mdx
<FatLink href="https://modrinth.com/plugin/plasmo-voice">Скачать Plasmo Voice</FatLink>
```

### Badge — бейджи

Цвета: `green`, `blue`, `yellow`, `red`, `purple`. Варианты: `outline` (по умолчанию), `filled`.

```mdx
<Badge color="green">Онлайн</Badge>
<Badge color="red" variant="filled">Оффлайн</Badge>
```

### BadgeGroup — группировка бейджей

```mdx
<BadgeGroup>
<Badge color="green">Java</Badge>
<Badge color="blue">Bedrock</Badge>
</BadgeGroup>
```

### CraftGrid — рецепты крафта

Имена предметов — snake_case ID из Minecraft. Иконки с `mc.nerothe.com`.

```mdx
<CraftGrid>
<CraftSlots>
<CraftSlot item="oak_planks" />
<CraftSlot item="oak_planks" />
<CraftSlot item="oak_planks" />
<CraftSlot />
<CraftSlot item="stick" />
<CraftSlot />
<CraftSlot />
<CraftSlot item="stick" />
<CraftSlot />
</CraftSlots>
<CraftArrow />
<CraftResult item="wooden_pickaxe" />
</CraftGrid>
```

### CommandTableFilter — таблица команд с поиском

```mdx
<CommandTableFilter>

| Команда | Описание |
|---------|----------|
| /spawn | Телепортация на спавн |
| /home | Телепортация домой |

</CommandTableFilter>
```

### AnimatedMedia — видео/анимации

Автоплей + луп для видео (mp4, webm). Для gif/webp — обычное изображение.

```mdx
<AnimatedMedia src="/assets/demo.mp4" alt="Демо" />
<AnimatedMedia src="/assets/animation.gif" width="400px" />
```

### InlineSpoiler — скрытый текст

```mdx
Ответ: <InlineSpoiler>42</InlineSpoiler>
```

### Grid — сетка изображений

```mdx
<Grid>

![](/assets/image1.png)
![](/assets/image2.png)

</Grid>
```

### kbd — клавиши

```mdx
Нажмите :kbd[Ctrl] + :kbd[Shift] + :kbd[P]
```

### figure / figcaption — изображение с подписью

```mdx
<figure>

![](/assets/screenshot.png)

:figcaption[Подпись к изображению]

</figure>
```

## Код

Блоки кода с подсветкой синтаксиса (Shiki). Указывайте язык:

````mdx
```python
def hello():
    print("Hello")
```
````

Инлайн-код: `` `команда` ``

## Таблицы

```mdx
| Колонка 1 | Колонка 2 |
|-----------|-----------|
| Ячейка    | Ячейка    |
```

## Изображения

Картинки в `assets/`, путь начинается с `/assets/`:

```mdx
![Описание](/assets/getting-started/screenshot.png)
```

## Тестовая страница

На dev-окружении доступна `/wiki/test` со всеми компонентами.
