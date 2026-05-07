# PRDX RP Сервер — Полный список внутриигровых фич

**Дата:** 2026-03-02
**Назначение:** Тест, GIF-стенды, планирование реализации

---

## СУЩЕСТВУЮЩИЕ — ТЕСТ + GIF СТЕНДЫ

### Чат (MurChat + BetterChatBubbles + Murcord)
| # | Стенд | Что показать в одной GIF |
|---|-------|--------------------------|
| 1 | Каналы чата | Локальный → `!`глобальный → `@`командный, `/cc` переключение |
| 2 | Личные сообщения | `/msg`, `/r` — диалог двух игроков |
| 3 | Спец-синтаксис | `:loc:` и `:item:` в одном сообщении |
| 4 | Пузыри | BetterChatBubbles — написать в локальный чат, пузырь над головой |
| 5 | Discord ↔ игра | Сообщение из #игра в Minecraft и обратно (Murcord) |

### RP-команды
| # | Стенд | Что показать |
|---|-------|-------------|
| 6 | RP-команды | `/me`, `/try`, `/do` в одной RP сцене с двумя игроками |
| 7 | `/gme` | Отдельно — видно всему серверу |
| 8 | Mention | Написать ник → подсветка + звук |

### Действия персонажа
| # | Стенд | Что показать |
|---|-------|-------------|
| 9 | Позы (GSit) | `/sit`, `/lay`, `/bellyflop`, `/crawl`, `/spin` + RMB на лестницу |
| 10 | Hat + Spit | `/hat` с 2-3 предметами + `/spit` с бутылкой |
| 11 | Наручники | Один игрок надевает на другого, эффекты |
| 12 | Emotecraft | 2-3 анимации эмоций |
| 13 | ArmorStand редактор | Деревянная мотыга → меню → поза → результат |

### Голос (PlasmoVoice + аддоны)
| # | Стенд | Что показать |
|---|-------|-------------|
| 14 | Базовый голос | Push-to-talk (V) + шёпот (Ctrl+V) + приоритет (Shift+V) |
| 15 | Группы голоса | Создание группы, приглашение, разговор |
| 16 | Sculk от голоса | Говорить рядом с sculk sensor → реакция |
| 17 | Пластинки / козий рог | Запись и воспроизведение (pv-addon-discs) |

### Миры и порталы
| # | Стенд | Что показать |
|---|-------|-------------|
| 18 | ArtWorld | Дыхание + плач. обсидиан → врата → переход → обратно → Shift+LMB удаление |
| 19 | FrogDisplays | Алмазная кирка по чёрному бетону → `/display create` → `/display video <URL>` |
| 20 | LinkedPortals | Зажигалка по рамке из плач. обсидиана → портал → переход в farmworld |
| 21 | End Portal | Вход в End → выход обратно (TheEndTeleport) |
| 22 | Кросс-сервер респавн | Кровать на farmworld → смерть в overworld → респавн на farmworld |

### Механики
| # | Стенд | Что показать |
|---|-------|-------------|
| 23 | Невидимые рамки + свет | Обычная vs невидимая рамка + невидимый свет в комнате |
| 24 | Дюпликация (Mosquito) | Поршневой дюп carpet/rail/sand |
| 25 | Villager Trade Rebalance | Торговля с жителем — новая система |
| 26 | OreAnnouncer | Добыча алмаза → алерт + `/oa stats` |
| 27 | BreweryX | Ферментация → дистилляция → выдержка → напиток (добавляется сейчас) |
| 28 | ChildrenMobs | Маленькие мобы |
| 29 | Снежки | Бросок → отброс игрока (подтверждено) |
| 30 | Скины | `/skin set` → `/skin url` → `/skin clear` |

### Карта + Таб
| # | Стенд | Что показать |
|---|-------|-------------|
| 31 | squaremap | Веб-карта + показать/скрыть себя |
| 32 | Velocitab | Таб с рангами и форматированием |

**Итого стендов: 32**

---

## В РАЗРАБОТКЕ

| # | Фича | Roadmap | Что решить |
|---|-------|---------|-----------|
| 33 | Ресурспак PRDX (через мод) | [#8](https://github.com/digitaldrugstech/prdx-roadmap/issues/8) P2 | Формат доставки, контент: тотемы, иконки, ранги |
| 34 | RP персонажи / Characters Service v2 | [#35](https://github.com/digitaldrugstech/prdx-roadmap/issues/35) P2 | Макс. персонажей, данные, переключение |
| 35 | РП Роли + маця роса | [#36](https://github.com/digitaldrugstech/prdx-roadmap/issues/36) P2 | Assigned: Komo4ekoI |
| 36 | Банковская система (сервис + плагин + сайт) | [#4](https://github.com/digitaldrugstech/prdx-roadmap/issues/4) P1 | Валюта, интерфейс, штрафы, карты, аренда меток |
| 37 | Штрафы (через банк) | [#59](https://github.com/digitaldrugstech/prdx-roadmap/issues/59) P1 | Blocked: зависит от банка |
| 38 | Маркеры + Team tags в чате | — | Формат `:m1:`, `:tTEAM:`, привязка к координатам |
| 39 | Limbo gameplay | — | Цель мира, квесты, как попасть |
| 40 | MarX — марки на сайте | [#10](https://github.com/digitaldrugstech/prdx-roadmap/issues/10) P2 | Сервис + плагин интеграция |
| 41 | Кастомные ачивки | [#37](https://github.com/digitaldrugstech/prdx-roadmap/issues/37) P2 | Assigned: whynotfu |
| 42 | Наручники — переписать плагин | [#6](https://github.com/digitaldrugstech/prdx-roadmap/issues/6) P1 | Старый D3st0ny → свой плагин |

## ЗАПЛАНИРОВАНО — НУЖНА РЕАЛИЗАЦИЯ

### P1 — Critical for season
| # | Фича | Roadmap | Что решить |
|---|-------|---------|-----------|
| 43 | Сигарета — РП предмет | [#44](https://github.com/digitaldrugstech/prdx-roadmap/issues/44) P1 | Кастом плагин, крафт/покупка, частицы, прогресс-бар, окурки |
| 44 | Дубинка для интерпола | [#45](https://github.com/digitaldrugstech/prdx-roadmap/issues/45) P1 | Эффект, длительность, permission для ОСН |
| 45 | Головы игроков в wandering trader | [#46](https://github.com/digitaldrugstech/prdx-roadmap/issues/46) P1 | Цена, механика |
| 46 | Улучшить невидимый свет (уровни 0-15) | [#47](https://github.com/digitaldrugstech/prdx-roadmap/issues/47) P1 | UI выбора яркости |
| 47 | Эндермены не берут блоки | [#48](https://github.com/digitaldrugstech/prdx-roadmap/issues/48) P1 | Вынести на МКО голосование |
| 48 | Порядочность / Вежливость (behavior score) | [#60](https://github.com/digitaldrugstech/prdx-roadmap/issues/60) P1 | Как в Dota, needs-spec |
| 49 | Интеграция общин и структур (MC + Discord + сайт) | [#7](https://github.com/digitaldrugstech/prdx-roadmap/issues/7) P1 | needs-spec |
| 50 | Brewery и плагинслоп | [#5](https://github.com/digitaldrugstech/prdx-roadmap/issues/5) P1 | Assigned: thehaffk, рецепты и конфиг |

### P2 — Important
| # | Фича | Roadmap | Что решить |
|---|-------|---------|-----------|
| 51 | `^ping` в чате | — | Формат, MurChat интеграция |
| 52 | Редактирование предметов | [#53](https://github.com/digitaldrugstech/prdx-roadmap/issues/53) P2 | Формат TBD (не /rename /lore) |
| 53 | Патенты (защита артов) | [#54](https://github.com/digitaldrugstech/prdx-roadmap/issues/54) P2 | Регистрация, проверка, права |
| 54 | Кальян | [#51](https://github.com/digitaldrugstech/prdx-roadmap/issues/51) P2 | Варочная стойка + зелье → дым, привязка к BreweryX? |
| 55 | Демо режим (2 часа adventure) | [#40](https://github.com/digitaldrugstech/prdx-roadmap/issues/40) P2 | Как ограничить, что доступно |
| 56 | Картинки в игровом чате (Discord ↔ MC) | [#9](https://github.com/digitaldrugstech/prdx-roadmap/issues/9) P2 | Формат отображения |
| 57 | Мячи на сервере | [#11](https://github.com/digitaldrugstech/prdx-roadmap/issues/11) P2 | Assigned: apehum |
| 58 | /spit улучшения | [#12](https://github.com/digitaldrugstech/prdx-roadmap/issues/12) P2 | Текущий плагин basic, нужно допилить |
| 59 | Судебная система | [#14](https://github.com/digitaldrugstech/prdx-roadmap/issues/14) P2 | Техническая реализация, needs-spec |
| 60 | Процедуры | [#18](https://github.com/digitaldrugstech/prdx-roadmap/issues/18) P2 | needs-spec |
| 61 | Сборка | [#38](https://github.com/digitaldrugstech/prdx-roadmap/issues/38) P2 | — |
| 62 | Новые админ утилиты (/gtp, etc) | [#41](https://github.com/digitaldrugstech/prdx-roadmap/issues/41) P2 | Список утилит |

### P3 — Nice to have
| # | Фича | Roadmap | Что решить |
|---|-------|---------|-----------|
| 63 | Клешня краба (увелич. дистанция блоков) | [#50](https://github.com/digitaldrugstech/prdx-roadmap/issues/50) P3 | Сколько блоков, крафт |
| 64 | Мини-механики: кора, наковальня, костёр, стук, подпись | [#52](https://github.com/digitaldrugstech/prdx-roadmap/issues/52) P3 | Datapack или плагин |
| 65 | Новые осады (рейды) | [#43](https://github.com/digitaldrugstech/prdx-roadmap/issues/43) P3 | korobkaidea |
| 66 | Деревни христиан | [#42](https://github.com/digitaldrugstech/prdx-roadmap/issues/42) P3 | korobkaidea |
| 67 | TRVZ Calls | [#20](https://github.com/digitaldrugstech/prdx-roadmap/issues/20) P3 | needs-spec |
