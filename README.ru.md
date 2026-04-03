> [English version](README.md)

# claude-skills-kit

![GitHub stars](https://img.shields.io/github/stars/KirKruglov/claude-skills-kit?style=flat-square)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](LICENSE)
![Skills](https://img.shields.io/badge/skills-11-informational?style=flat-square)


Растущая коллекция переиспользуемых скиллов для Claude — готовые файлы с инструкциями, которые расширяют поведение Claude в любом интерфейсе: Claude.ai, Claude Projects, API или Cowork.

---

## Что такое скилл?

Скилл — это папка с файлом `SKILL.md`, содержащим структурированные инструкции для Claude. Добавь его в Claude.ai или Cowork — и Claude получает новую, воспроизводимую возможность без написания кода.

Скиллы:
- **Независимы от интерфейса** — работают в Claude.ai, Projects, API и Cowork
- **Самодостаточны** — каждая папка скилла содержит всё необходимое
- **Компонуемы** — несколько скиллов можно объединить в одной настройке

---

## Скиллы

Каждый скилл доступен в двух языковых версиях. Claude активирует скилл на основе языка запроса — используй EN-версию для английского, RU-версию для русского.

Пример: RU-версия `prompt-builder` запускается по триггеру **"напиши промт"**, EN-версия — по **"create a prompt"**.

| Скилл | EN | RU | Описание |
|-------|----|----|----------|
| context-builder-cowork | [EN](skills/context-builder-cowork/) | [RU](skills/context-builder-cowork-ru/) | Генерирует структурированный `project-context.md` через интерактивное интервью |
| prompt-builder | [EN](skills/prompt-builder/) | [RU](skills/prompt-builder-ru/) | Создаёт структурированный промпт для любой задачи через серию вопросов |
| report-analyzer | [EN](skills/report-analyzer/) | [RU](skills/report-analyzer-ru/) | Анализирует большие отчёты (PDF/PPTX) и формирует структурированное резюме с ключевыми данными и инсайтами |
| project-onboarding | [EN/RU](skills/project-onboarding/) | — | Полный онбординг проекта в Cowork: генерирует context.md, правила папки, карту файлов и стартовые промпты за одну сессию. Двуязычный EN/RU |
| project-management-kit | [Подробнее](skills/project-management-kit/) | — | AI-агент для управления проектами — 7 скиллов для проектной документации (устав, реестр рисков, план проекта, план коммуникаций, протокол встречи, отчёт план/факт, отчёт о закрытии). PMBoK 8 + Agile. Двуязычный EN/RU |

Новые скиллы будут добавляться.

---

## Структура репозитория

```
claude-skills-kit/
├── skills/
│   ├── context-builder-cowork/       # EN
│   │   └── SKILL.md
│   ├── context-builder-cowork-ru/    # RU
│   │   └── SKILL.md
│   ├── prompt-builder/               # EN
│   │   └── SKILL.md
│   ├── prompt-builder-ru/            # RU
│   │   └── SKILL.md
│   ├── report-analyzer/              # EN
│   │   └── SKILL.md, README.md, ...
│   ├── report-analyzer-ru/           # RU
│   │   └── SKILL.md, README.md, ...
│   ├── project-onboarding/           # EN/RU (двуязычный)
│   │   ├── SKILL.md
│   │   ├── README.md
│   │   ├── README.ru.md
│   │   └── resources/
│   └── project-management-kit/       # Набор скиллов (EN/RU)
│       ├── README.md
│       ├── system-prompt.md
│       ├── project-instructions.md
│       ├── docs/                     # INSTALL, USER-GUIDE
│       ├── generate-charter/         # 7 скиллов, каждый с
│       ├── generate-risk-register/   #   SKILL.md, README.md,
│       ├── generate-project-plan/    #   README.ru.md, templates/
│       ├── generate-comm-plan/
│       ├── generate-meeting-protocol/
│       ├── generate-plan-fact-report/
│       └── generate-closure-report/
├── README.md
└── README.ru.md
```

---

## Как установить скилл

### Вариант 1 — Git clone (рекомендуется)

```bash
git clone https://github.com/KirKruglov/claude-skills-kit.git
```

Нужная папка скилла будет по пути `skills/skill-name/`.

### Вариант 2 — Скачать папку одного скилла

1. Открой папку скилла в репозитории
2. Скачай файл `SKILL.md`
3. Создай локальную папку с именем скилла (например, `context-builder-cowork`)
4. Положи `SKILL.md` внутрь этой папки

---

## Как добавить скилл в Claude.ai

> Требуется план Pro, Max, Team или Enterprise с включённым Code Execution.

1. Перейди в **Settings → Capabilities** и убедись, что **Code Execution and File Creation** включён
2. Возьми папку скилла (например, `context-builder-cowork/`) и сожми её в ZIP-файл
   - ZIP должен содержать саму папку как корень, а не файлы внутри неё напрямую
3. Перейди в **Customize → Skills**
4. Нажми **"+"** → **"Upload a skill"**
5. Выбери ZIP-файл
6. Скилл появится в списке — включи тогл

Claude будет автоматически активировать скилл, когда запрос соответствует его назначению.

---

## Как добавить скилл в Claude Cowork

1. Открой Claude Cowork (десктопное приложение)
2. Перейди в **Settings → Skills**
3. Нажми **"+"** → **"Upload a skill"**
4. Выбери ZIP-файл, подготовленный так же, как описано выше
5. Включи тогл

---

## Contributing

Скиллы публикуются и поддерживаются автором репозитория.

Чтобы предложить скилл или сообщить о проблеме — открой GitHub Issue с:
- Кратким описанием того, что делает скилл
- Примером триггерной фразы
- Ожидаемым результатом

Pull request'ы приветствуются после публикации гайдлайнов для контрибьюторов.

---

## Лицензия

MIT
