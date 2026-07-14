# Инструкция по установке

Пошаговая настройка AI-агента для управления проектами в Claude.ai.

## Предварительные требования

- **Подписка Claude Pro или Max** — необходима для функции Projects
- **Claude.ai Projects** — доступна на [claude.ai](https://claude.ai) в левой боковой панели

## Шаги установки

### Шаг 1. Создайте новый проект

1. Откройте [claude.ai](https://claude.ai).
2. В левой боковой панели нажмите **Projects** → **New Project**.
3. Назовите проект (например, «Project Manager Agent»).

### Шаг 2. Задайте инструкции проекта

1. Откройте настройки проекта.
2. В поле **Project Instructions** вставьте содержимое файла `project-instructions.md`.
3. Сохраните.

Это основной промпт, который определяет поведение Claude как менеджера проектов.

### Шаг 3. Загрузите файлы знаний

Загрузите следующие файлы в раздел **Knowledge** проекта. Порядок важен — загружайте в указанной последовательности.

**Обязательные файлы:**

| # | Файл | Назначение |
|---|------|------------|
| 1 | `system-prompt.md` | Полная инструкция агента: протокол задач, скиллы, структура файлов, правила коммуникации |
| 2 | `skills/generate-charter/SKILL.md` | Скилл: генерация устава проекта |
| 3 | `skills/generate-charter/templates/project-charter-en.md` | Шаблон: устав (EN) |
| 4 | `skills/generate-charter/templates/project-charter-ru.md` | Шаблон: устав (RU) |
| 5 | `skills/generate-risk-register/SKILL.md` | Скилл: генерация реестра рисков |
| 6 | `skills/generate-risk-register/templates/risk-register-en.md` | Шаблон: реестр рисков (EN) |
| 7 | `skills/generate-risk-register/templates/risk-register-ru.md` | Шаблон: реестр рисков (RU) |
| 8 | `skills/generate-project-plan/SKILL.md` | Скилл: генерация плана проекта |
| 9 | `skills/generate-project-plan/templates/project-plan-en.md` | Шаблон: план проекта (EN) |
| 10 | `skills/generate-project-plan/templates/project-plan-ru.md` | Шаблон: план проекта (RU) |
| 11 | `skills/generate-comm-plan/SKILL.md` | Скилл: генерация плана коммуникаций |
| 12 | `skills/generate-comm-plan/templates/comm-plan-en.md` | Шаблон: план коммуникаций (EN) |
| 13 | `skills/generate-comm-plan/templates/comm-plan-ru.md` | Шаблон: план коммуникаций (RU) |
| 14 | `skills/generate-meeting-protocol/SKILL.md` | Скилл: генерация протокола встречи |
| 15 | `skills/generate-meeting-protocol/templates/meeting-protocol-en.md` | Шаблон: протокол встречи (EN) |
| 16 | `skills/generate-meeting-protocol/templates/meeting-protocol-ru.md` | Шаблон: протокол встречи (RU) |
| 17 | `skills/generate-plan-fact-report/SKILL.md` | Скилл: отчёт план/факт |
| 18 | `skills/generate-plan-fact-report/templates/plan-fact-report-en.md` | Шаблон: отчёт план/факт (EN) |
| 19 | `skills/generate-plan-fact-report/templates/plan-fact-report-ru.md` | Шаблон: отчёт план/факт (RU) |
| 20 | `skills/generate-closure-report/SKILL.md` | Скилл: генерация отчёта о закрытии |
| 21 | `skills/generate-closure-report/templates/closure-report-en.md` | Шаблон: отчёт о закрытии (EN) |
| 22 | `skills/generate-closure-report/templates/closure-report-ru.md` | Шаблон: отчёт о закрытии (RU) |

**Опциональные файлы (улучшают непрерывность между сессиями):**

| Файл | Назначение |
|------|------------|
| `project-state.md` | Реестр статусов артефактов — помогает агенту понять, какие документы уже утверждены |

### Шаг 4. Проверьте установку

Начните новый чат в проекте и отправьте:

```
Сформируй устав проекта. Бриф: разрабатываем мобильное приложение для трекинга фитнес-целей. Сроки: 4 месяца. Бюджет: $50,000. Команда: 1 PM, 2 разработчика, 1 дизайнер, 1 QA.
```

**Ожидаемое поведение:**

1. Агент читает `system-prompt.md` и скилл генерации устава.
2. Может задать уточняющие вопросы (стейкхолдеры, ограничения, критерии успеха).
3. Генерирует структурированный устав по шаблону.
4. Представляет результат и запрашивает подтверждение.

Если агент не следует шаблону или игнорирует инструкции скилла — проверьте, что все файлы знаний загружены корректно.

## Структура файлов

```
project-name/
├── system-prompt.md          — полная инструкция агента
├── project-instructions.md   — компактный промпт для поля Project Instructions
├── skills/
│   └── {skill-name}/
│       ├── SKILL.md           — алгоритм скилла
│       └── templates/
│           ├── {name}-en.md   — шаблон (EN)
│           └── {name}-ru.md   — шаблон (RU)
├── input/                     — данные вашего проекта (бриф, ответы, ограничения)
├── output/                    — документы, сгенерированные агентом
├── logs/
│   └── log.md                 — лог проекта
└── project-state.md           — реестр статусов артефактов
```

## Решение проблем

**Агент игнорирует инструкции скилла.** Самая частая причина — файл SKILL.md не загружен в Knowledge. Проверьте наличие всех файлов в разделе Knowledge проекта.

**Агент выдаёт неструктурированный результат.** Убедитесь, что `system-prompt.md` загружен. Он содержит протокол выполнения задач, обеспечивающий структурированный вывод.

**Агент отвечает на неправильном языке.** Агент определяет язык по вашему сообщению. Пишете на русском — отвечает на русском. Чтобы сменить язык, напишите следующее сообщение на нужном языке.

**Достигнут лимит файлов знаний.** В Claude.ai Projects есть ограничение на количество файлов знаний. При достижении лимита приоритеты: сначала `system-prompt.md`, затем файлы скиллов для текущей фазы. Файлы скиллов можно менять между фазами.

## Далее

Подробные сценарии использования, примеры команд и рекомендации — в [Руководстве пользователя](USER-GUIDE.ru.md).
