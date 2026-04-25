> [English version](INSTALL.md)

# Как установить скилл

Пошаговая инструкция по получению скилла и добавлению его в Claude.

---

## Часть 1 — Получить файлы скилла

Выбери любой подходящий вариант.

### Вариант 1 — Git clone (весь набор)

```bash
git clone https://github.com/KirKruglov/claude-skills-kit.git
```

Все папки скиллов будут по пути `skills/<skill-name>/`.

### Вариант 2 — Git sparse-checkout (один скилл, без полного клонирования)

```bash
git clone --filter=blob:none --sparse https://github.com/KirKruglov/claude-skills-kit.git
cd claude-skills-kit
git sparse-checkout set skills/<skill-name>
```

Для скиллов внутри `project-management-kit` используй вложенный путь:

```bash
git sparse-checkout set skills/project-management-kit/generate-charter
```

### Вариант 3 — Скачать через браузер, без CLI

Открой в браузере (замени `<skill-name>` на реальное имя папки):

```
https://download-directory.github.io/?url=https://github.com/KirKruglov/claude-skills-kit/tree/main/skills/<skill-name>
```

Скачается ZIP только с нужной папкой скилла. Рекомендуется нетехническим пользователям.

### Вариант 4 — Один файл `SKILL.md` через curl

```bash
curl -O https://raw.githubusercontent.com/KirKruglov/claude-skills-kit/main/skills/<skill-name>/SKILL.md
```

Или: открой файл на GitHub → нажми **Raw** → **Сохранить как** в браузере.

### Вариант 5 — ZIP всего репозитория через GitHub UI

GitHub → **Code** → **Download ZIP** → распакуй нужную папку скилла.

Самый простой вариант, но скачивает весь репозиторий.

---

## Часть 2 — Добавить в свою платформу

### Claude.ai — Projects (рекомендуется, любой тариф)

1. Открой [claude.ai](https://claude.ai) и войди в аккаунт
2. Нажми **Projects** в левой панели
3. Открой или создай проект
4. Нажми иконку **Project settings** → **Custom instructions**
5. Скопируй всё содержимое файла `SKILL.md` скилла и вставь в поле
6. Нажми **Save**
7. Начни новый диалог внутри проекта — скилл активен

### Claude.ai — вкладка Skills (загрузка ZIP)

> Требуется тариф Pro, Max, Team или Enterprise с включённым Code Execution.

1. Перейди в **Settings → Capabilities** и включи **Code Execution and File Creation**
2. Сожми папку скилла в ZIP-файл — папка должна быть корнем ZIP, а не файлы напрямую
3. Перейди в **Customize → Skills** → **"+"** → **"Upload a skill"**
4. Выбери ZIP-файл
5. Включи тогл — Claude будет автоматически активировать скилл при совпадении запроса

### Claude Cowork

**Вариант A — автоопределение (рекомендуется):**
Скопируй папку скилла в рабочую директорию Cowork. Claude обнаружит его автоматически.

**Вариант B — ручная загрузка:**
1. Открой Claude Cowork (десктопное приложение)
2. Перейди в **Settings → Skills** → **"+"** → **"Upload a skill"**
3. Выбери ZIP-файл, подготовленный так же, как описано в разделе Skills выше
4. Включи тогл

---

## Решение проблем

| Проблема | Решение |
|----------|---------|
| Скилл не активируется | Убедись, что скопировал **весь** файл `SKILL.md`, включая YAML-заголовок в начале |
| Поведение отличается от описания в README | Некоторые скиллы предназначены для конкретной платформы — проверь `README.md` скилла |
| Неправильный язык | Скиллы поддерживают EN и RU — попробуй триггерную фразу на другом языке |
| Сообщение «инструмент недоступен» в Claude.ai | Скилл автоматически переключится в режим только чтения — это ожидаемое поведение в ряде сред |
