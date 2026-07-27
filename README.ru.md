> [English version](README.md)

# claude-skills-kit

![GitHub stars](https://img.shields.io/github/stars/KirKruglov/claude-skills-kit?style=flat-square)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](LICENSE)
![Skills](https://img.shields.io/badge/skills-77-informational?style=flat-square)
![Last commit](https://img.shields.io/github/last-commit/KirKruglov/claude-skills-kit?style=flat-square)

77 готовых скилл-агентов для Claude — созданы для нетехнических специалистов в командах продукта, операций, финансов, HR и отраслевых направлений.

> 70 отдельных скиллов + 7 вложенных скиллов в `project-management-kit`

---

## Быстрый старт

**Шаг 1.** Найди скилл в каталоге ниже.

**Шаг 2.** Скопируй папку скилла в своё рабочее пространство:

- **Cowork** — скопируй папку скилла в рабочую директорию Cowork. Claude обнаружит его автоматически.
- **Claude.ai / Projects** — открой `SKILL.md` скилла, скопируй содержимое и вставь в Project Instructions.

**Шаг 3.** Используй Claude как обычно. Скилл активируется по сообщению — команды не нужны.

> Пошаговая инструкция по установке — в [INSTALL.ru.md](INSTALL.ru.md) / [INSTALL.md](INSTALL.md).

---

## Почему Claude Skills Kit?

Большинство репозиториев скиллов содержат только файл `SKILL.md`.
Claude Skills Kit поставляет **полный пакет** для каждого скилла:

| Что включено                     | Зачем это нужно                                            |
| -------------------------------- | ---------------------------------------------------------- |
| `SKILL.md` — основные инструкции | Claude активирует скилл                                    |
| `README.md` (EN + RU)            | Ты знаешь, что делает скилл, до установки                  |
| `docs/USER-GUIDE.md`             | Как использовать скилл с примерами (где применимо)         |
| `INSTALL.md` (EN + RU)           | Общая инструкция по установке — в корне репозитория        |

**Создан для нетехнических пользователей.** Никакого кода, CLI и конфигурации.
**Двуязычный EN/RU.** Claude определяет язык запроса автоматически.

---

## Что такое скилл?

Скилл — это папка с файлом `SKILL.md`, содержащим структурированные инструкции для Claude. Добавь его в Claude.ai или Cowork — и Claude получает новую, воспроизводимую возможность без написания кода.

Скиллы:
- **Независимы от интерфейса** — работают в Claude.ai, Projects, API и Cowork
- **Самодостаточны** — каждая папка скилла содержит всё необходимое
- **Компонуемы** — несколько скиллов можно объединить в одной настройке

---

## Найти по роли

Один скилл может встречаться в нескольких ролях. Полные описания — в [каталоге ниже](#скиллы).

**📆 PM / Продакт** — [project-management-kit](skills/project-management/project-management-kit/) · [project-onboarding](skills/project-management/project-onboarding/) · [context-builder-cowork](skills/project-management/context-builder-cowork/) · [sprint-review-summarizer](skills/project-management/sprint-review-summarizer/) · [backlog-grooming-assistant](skills/project-management/backlog-grooming-assistant/) · [retro-pattern-analyzer](skills/project-management/retro-pattern-analyzer/) · [decision-log](skills/project-management/decision-log/) · [weekly-digest-synthesizer](skills/status-reports-and-stakeholder-updates/weekly-digest-synthesizer/) · [okr-progress-narrator](skills/status-reports-and-stakeholder-updates/okr-progress-narrator/) · [stakeholder-adapter](skills/status-reports-and-stakeholder-updates/stakeholder-adapter/) · [meeting-prep-briefer](skills/team-leadership/meeting-prep-briefer/) · [user-feedback-synthesizer](skills/discovery-and-user-research/user-feedback-synthesizer/) · [user-persona-synthesizer](skills/discovery-and-user-research/user-persona-synthesizer/) · [jobs-to-be-done-extractor](skills/discovery-and-user-research/jobs-to-be-done-extractor/) · [prd-review-challenger](skills/launch-and-releases/prd-review-challenger/) · [release-notes-generator](skills/launch-and-releases/release-notes-generator/) · [feature-announcement-writer](skills/launch-and-releases/feature-announcement-writer/) · [changelog-narrator](skills/launch-and-releases/changelog-narrator/) · [survey-results-analyzer](skills/launch-and-releases/survey-results-analyzer/) · [retention-cohort-interpreter](skills/data-analysis/retention-cohort-interpreter/) · [experiment-results-interpreter](skills/data-analysis/experiment-results-interpreter/) · [north-star-metric-auditor](skills/metrics-and-exec-narratives/north-star-metric-auditor/) · [competitive-feature-matrix-builder](skills/market-and-competitive-intelligence/competitive-feature-matrix-builder/) · [weekly-competitor-tracker](skills/market-and-competitive-intelligence/weekly-competitor-tracker/) · [industry-trend-brief](skills/market-and-competitive-intelligence/industry-trend-brief/) · [research-folder-synthesizer](skills/personal-productivity/research-folder-synthesizer/) · [reading-list-prioritizer](skills/personal-productivity/reading-list-prioritizer/)

**🚀 Founder / CEO** — [exec-metrics-storyteller](skills/metrics-and-exec-narratives/exec-metrics-storyteller/) · [weekly-metrics-story-writer](skills/metrics-and-exec-narratives/weekly-metrics-story-writer/) · [north-star-metric-auditor](skills/metrics-and-exec-narratives/north-star-metric-auditor/) · [fundraise-pipeline-tracker](skills/business-ops/fundraise-pipeline-tracker/) · [data-room-prep-checklist](skills/business-ops/data-room-prep-checklist/) · [proposal-and-quote-drafter](skills/business-ops/proposal-and-quote-drafter/) · [win-loss-debrief-writer](skills/business-ops/win-loss-debrief-writer/) · [company-policy-drafter](skills/business-ops/company-policy-drafter/) · [job-description-and-scorecard-builder](skills/hiring-and-hr/job-description-and-scorecard-builder/) · [onboarding-plan-30-60-90](skills/hiring-and-hr/onboarding-plan-30-60-90/) · [invoice-and-payment-tracker-summary](skills/finance-and-billing/invoice-and-payment-tracker-summary/) · [accounts-receivable-followup-writer](skills/finance-and-billing/accounts-receivable-followup-writer/) · [monthly-close-checklist-and-reconciliation-prep](skills/finance-and-billing/monthly-close-checklist-and-reconciliation-prep/) · [competitive-feature-matrix-builder](skills/market-and-competitive-intelligence/competitive-feature-matrix-builder/) · [industry-trend-brief](skills/market-and-competitive-intelligence/industry-trend-brief/) · [daily-admin-brief](skills/personal-productivity/daily-admin-brief/)

**👥 Team Lead / Руководитель** — [one-to-one-prep](skills/team-leadership/one-to-one-prep/) · [delegation-brief](skills/team-leadership/delegation-brief/) · [meeting-prep-briefer](skills/team-leadership/meeting-prep-briefer/) · [team-update-aggregator](skills/status-reports-and-stakeholder-updates/team-update-aggregator/) · [morning-standup-brief-generator](skills/status-reports-and-stakeholder-updates/morning-standup-brief-generator/) · [weekly-status-report-generator](skills/status-reports-and-stakeholder-updates/weekly-status-report-generator/) · [weekly-digest-synthesizer](skills/status-reports-and-stakeholder-updates/weekly-digest-synthesizer/) · [okr-progress-narrator](skills/status-reports-and-stakeholder-updates/okr-progress-narrator/) · [decision-log](skills/project-management/decision-log/) · [hiring-pipeline-reviewer](skills/hiring-and-hr/hiring-pipeline-reviewer/) · [onboarding-plan-30-60-90](skills/hiring-and-hr/onboarding-plan-30-60-90/) · [interview-debrief-synthesizer](skills/hiring-and-hr/interview-debrief-synthesizer/) · [workspace-health-monitor](skills/personal-productivity/workspace-health-monitor/) · [daily-admin-brief](skills/personal-productivity/daily-admin-brief/)

**🧑‍💼 HR / Рекрутер** — [hiring-pipeline-reviewer](skills/hiring-and-hr/hiring-pipeline-reviewer/) · [job-description-and-scorecard-builder](skills/hiring-and-hr/job-description-and-scorecard-builder/) · [onboarding-plan-30-60-90](skills/hiring-and-hr/onboarding-plan-30-60-90/) · [interview-debrief-synthesizer](skills/hiring-and-hr/interview-debrief-synthesizer/) · [company-policy-drafter](skills/business-ops/company-policy-drafter/)

**💰 Finance / Ops** — [invoice-and-payment-tracker-summary](skills/finance-and-billing/invoice-and-payment-tracker-summary/) · [accounts-receivable-followup-writer](skills/finance-and-billing/accounts-receivable-followup-writer/) · [monthly-close-checklist-and-reconciliation-prep](skills/finance-and-billing/monthly-close-checklist-and-reconciliation-prep/) · [legal-matter-tracker](skills/business-ops/legal-matter-tracker/)

**📣 Marketer** — [campaign-retrospective-writer](skills/marketing-and-content/campaign-retrospective-writer/) · [content-performance-reporter](skills/marketing-and-content/content-performance-reporter/) · [research-to-content-brief](skills/marketing-and-content/research-to-content-brief/) · [feature-announcement-writer](skills/launch-and-releases/feature-announcement-writer/) · [release-notes-generator](skills/launch-and-releases/release-notes-generator/) · [newsletter-digest-builder](skills/personal-productivity/newsletter-digest-builder/) · [reading-list-prioritizer](skills/personal-productivity/reading-list-prioritizer/) · [industry-trend-brief](skills/market-and-competitive-intelligence/industry-trend-brief/) · [weekly-competitor-tracker](skills/market-and-competitive-intelligence/weekly-competitor-tracker/) · [competitive-feature-matrix-builder](skills/market-and-competitive-intelligence/competitive-feature-matrix-builder/)

**📊 Analyst** — [csv-data-analyzer](skills/data-analysis/csv-data-analyzer/) · [report-analyzer](skills/data-analysis/report-analyzer/) · [retention-cohort-interpreter](skills/data-analysis/retention-cohort-interpreter/) · [experiment-results-interpreter](skills/data-analysis/experiment-results-interpreter/) · [metrics-anomaly-investigator](skills/data-analysis/metrics-anomaly-investigator/) · [kpi-digest-builder](skills/metrics-and-exec-narratives/kpi-digest-builder/) · [exec-metrics-storyteller](skills/metrics-and-exec-narratives/exec-metrics-storyteller/) · [weekly-metrics-story-writer](skills/metrics-and-exec-narratives/weekly-metrics-story-writer/) · [north-star-metric-auditor](skills/metrics-and-exec-narratives/north-star-metric-auditor/) · [survey-results-analyzer](skills/launch-and-releases/survey-results-analyzer/) · [content-performance-reporter](skills/marketing-and-content/content-performance-reporter/) · [research-folder-synthesizer](skills/personal-productivity/research-folder-synthesizer/)

**🤖 Claude power user** — [prompt-builder](skills/prompts-and-memory/prompt-builder/) · [prompt-library-curator](skills/prompts-and-memory/prompt-library-curator/) · [memory-auditor-chat](skills/prompts-and-memory/memory-auditor-chat/) · [memory-auditor-cowork](skills/prompts-and-memory/memory-auditor-cowork/) · [session-handoff-composer](skills/sessions-and-context/session-handoff-composer/) · [context-window-health-check](skills/sessions-and-context/context-window-health-check/) · [cowork-session-planner](skills/sessions-and-context/cowork-session-planner/) · [feature-guide](skills/setup-and-audit/feature-guide/) · [cowork-plugin-audit](skills/setup-and-audit/cowork-plugin-audit/) · [skill-usage-log-reviewer](skills/setup-and-audit/skill-usage-log-reviewer/) · [routines-setup-assistant](skills/setup-and-audit/routines-setup-assistant/) · [weekly-ai-workflow-review](skills/setup-and-audit/weekly-ai-workflow-review/) · [setup-wizard](skills/setup-and-audit/setup-wizard/)

---

## Скиллы

Колонка **Input** показывает, что нужно подать на вход, чтобы скилл заработал.

| Домен | Группы |
| ----- | ------ |
| [I. Проекты и статусы](#i-проекты-и-статусы) | [Управление проектами](#управление-проектами) · [Статус-отчёты и апдейты](#статус-отчёты-и-апдейты) |
| [II. Люди](#ii-люди) | [Управление командой](#управление-командой) · [Найм и HR](#найм-и-hr) |
| [III. Продукт](#iii-продукт) | [Discovery и UX-исследования](#discovery-и-ux-исследования) · [Запуски и релизы](#запуски-и-релизы) |
| [IV. Данные](#iv-данные) | [Анализ данных](#анализ-данных) · [Метрики и отчёты для руководства](#метрики-и-отчёты-для-руководства) |
| [V. Бизнес](#v-бизнес) | [Конкуренты и рынок](#конкуренты-и-рынок) · [Маркетинг и контент](#маркетинг-и-контент) · [Business Ops](#business-ops) · [Финансы и счета](#финансы-и-счета) |
| [VI. Личное и Claude](#vi-личное-и-claude) | [Личная продуктивность](#личная-продуктивность) · [Промпты и память](#промпты-и-память) · [Сессии и контекст](#сессии-и-контекст) · [Настройка и аудит](#настройка-и-аудит) |

---

### I. Проекты и статусы

#### Управление проектами

| Скилл | Input | Ссылка | Описание |
| ----- | ----- | ------ | -------- |
| project-management-kit | Бриф проекта → 7 вложенных скиллов | [→](skills/project-management/project-management-kit/) | Набор скиллов для управления проектами — 7 скиллов для проектной документации (устав, реестр рисков, план проекта, план коммуникаций, протокол встречи, отчёт план/факт, отчёт о закрытии). PMBoK 8 + Agile. Двуязычный EN/RU |
| project-onboarding | Ответы на вопросы и папка | [→](skills/project-management/project-onboarding/) | Полный онбординг проекта в Cowork: генерирует context.md, правила папки, карту файлов и стартовые промпты за одну сессию. Двуязычный EN/RU |
| context-builder-cowork | Ответы на вопросы | [→](skills/project-management/context-builder-cowork/) | Генерирует структурированный `project-context.md` через интерактивное интервью |
| sprint-review-summarizer | Вставленные заметки спринта или .md | [→](skills/project-management/sprint-review-summarizer/) | Преобразует заметки на свободном языке в структурированный документ для стейкхолдеров — выполнено, перенесено, риски, фокус следующего спринта. Jira не нужен. Двуязычный EN/RU |
| backlog-grooming-assistant | Бэклог в CSV или Markdown | [→](skills/project-management/backlog-grooming-assistant/) | Читает локальный экспорт бэклога (CSV или Markdown), флагирует проблемные задачи (нет владельца, нет оценки, устаревшие, заблокированные) и формирует структурированную повестку груминга со scorecard. Jira API не нужен. Двуязычный EN/RU |
| retro-pattern-analyzer | Два и более файла ретро | [→](skills/project-management/retro-pattern-analyzer/) | Анализирует файлы ретроспектив нескольких спринтов и выявляет повторяющиеся боли, нерешённые action items и стабильные позитивные паттерны команды. Двуязычный EN/RU |
| decision-log | Вставленный текст встречи или треда | [→](skills/project-management/decision-log/) | Извлекает структурированные решения из заметок встреч, Slack-тредов или email-цепочек — ведёт чистый лог отдельно от action items. Два режима: новый лог и пополнение с дедупликацией. Двуязычный EN/RU |

##### Project Management Kit — 7 вложенных скиллов

| Скилл | Input | Ссылка | Описание |
| ----- | ----- | ------ | -------- |
| generate-charter | Бриф или свободные заметки | [→](skills/project-management/project-management-kit/generate-charter/) | Генерирует устав проекта — базовый документ фазы инициации. Двуязычный EN/RU |
| generate-risk-register | Утверждённый файл project-charter.md | [→](skills/project-management/project-management-kit/generate-risk-register/) | Генерирует или обновляет реестр рисков с оценкой вероятности/влияния и стратегиями реагирования. Двуязычный EN/RU |
| generate-project-plan | Утверждённый файл project-charter.md | [→](skills/project-management/project-management-kit/generate-project-plan/) | Генерирует план проекта с WBS, вехами, зависимостями и картой ресурсов. Двуязычный EN/RU |
| generate-comm-plan | Файлы project-charter.md и project-plan.md | [→](skills/project-management/project-management-kit/generate-comm-plan/) | Генерирует план коммуникаций с матрицей стейкхолдеров, расписанием и правилами эскалации. Двуязычный EN/RU |
| generate-meeting-protocol | Свободные заметки со встречи | [→](skills/project-management/project-management-kit/generate-meeting-protocol/) | Генерирует структурированный протокол встречи из свободных заметок. Двуязычный EN/RU |
| generate-plan-fact-report | project-plan.md и фактические данные | [→](skills/project-management/project-management-kit/generate-plan-fact-report/) | Генерирует отчёт план/факт — сравнение плановых и фактических данных проекта. Двуязычный EN/RU |
| generate-closure-report | Устав, план-факт отчёт, уроки | [→](skills/project-management/project-management-kit/generate-closure-report/) | Генерирует отчёт о закрытии проекта — итоговый артефакт жизненного цикла. Двуязычный EN/RU |

#### Статус-отчёты и апдейты

| Скилл | Input | Ссылка | Описание |
| ----- | ----- | ------ | -------- |
| weekly-digest-synthesizer | Папка с .md/.txt статусами | [→](skills/status-reports-and-stakeholder-updates/weekly-digest-synthesizer/) | Компилирует статусы из файлов .md/.txt в структурированный еженедельный дайджест по проектам, с задачами и блокерами. Двуязычный EN/RU |
| weekly-status-report-generator | Вставленные заметки за неделю | [→](skills/status-reports-and-stakeholder-updates/weekly-status-report-generator/) | Преобразует сырые заметки недели в два готовых статус-отчёта за один проход: развёрнутый для менеджера и краткий (3 пункта) для skip-level. Двуязычный EN/RU |
| team-update-aggregator | Папка с .md/.txt апдейтами сотрудников | [→](skills/status-reports-and-stakeholder-updates/team-update-aggregator/) | Агрегирует еженедельные обновления от членов команды в people-centric статус-отчёт — организованный по людям, а не по проектам. Прогресс, планы, блокеры, нагрузка и флаги внимания менеджера на каждого. Двуязычный EN/RU |
| morning-standup-brief-generator | Рабочая папка с .md/.txt заметками | [→](skills/status-reports-and-stakeholder-updates/morning-standup-brief-generator/) | Компилирует локальные заметки, задачи и проектные файлы в структурированный дейли-бриф — Вчера / Сегодня / Блокеры / Вопросы. Без коннекторов. Двуязычный EN/RU |
| okr-progress-narrator | Файл OKR (.md/.txt/.csv) или текст | [→](skills/status-reports-and-stakeholder-updates/okr-progress-narrator/) | Преобразует сырые OKR-данные (таблицы, списки, CSV или текст в чате) в нарративный апдейт для стейкхолдеров: executive summary, абзац по каждой цели, таблица KR, риски и следующие шаги. Двуязычный EN/RU |
| stakeholder-adapter | Исходный документ (.md/.txt или текст) | [→](skills/status-reports-and-stakeholder-updates/stakeholder-adapter/) | Адаптирует любой документ в версии для разных аудиторий: Руководство (бизнес-эффект, фокус на решениях), Команда (техническая глубина, actionable), Клиент (язык результатов, без жаргона). Двуязычный EN/RU |

---

### II. Люди

#### Управление командой

| Скилл | Input | Ссылка | Описание |
| ----- | ----- | ------ | -------- |
| one-to-one-prep | Заметки прошлого 1-on-1 и задачи | [→](skills/team-leadership/one-to-one-prep/) | Генерирует структурированный prep-документ для ежемесячных встреч 1-on-1: трекинг action items, приоритизированные темы, вопросы по мотивации. Двуязычный EN/RU |
| delegation-brief | Ответы на вопросы | [→](skills/team-leadership/delegation-brief/) | Генерирует структурированный бриф задачи через 5-вопросное интервью — готов к вставке в новый диалог Cowork. Двуязычный EN/RU |
| meeting-prep-briefer | Расписание дня и файлы workspace | [→](skills/team-leadership/meeting-prep-briefer/) | Генерирует структурированный бриф по каждой встрече дня — участники, контекст из локальных файлов, открытые вопросы и предлагаемая повестка. Вставьте расписание или укажите файл. Без интеграций. Двуязычный EN/RU |

#### Найм и HR

| Скилл | Input | Ссылка | Описание |
| ----- | ----- | ------ | -------- |
| hiring-pipeline-reviewer | Вставленные заметки по интервью | [→](skills/hiring-and-hr/hiring-pipeline-reviewer/) | Генерирует структурированный еженедельный статус по всем кандидатам пайплайна найма из заметок о собеседованиях и оценочных листов. Выявляет застрявших кандидатов, сводит оценки, формирует рекомендации. Двуязычный EN/RU |
| job-description-and-scorecard-builder | Вставленное описание роли | [→](skills/hiring-and-hr/job-description-and-scorecard-builder/) | Создаёт вакансию и согласованный оценочный лист для интервью по заметкам о роли — парная связка документов для менеджеров, ведущих найм без рекрутера. Без рекрутингового SaaS. Двуязычный EN/RU |
| onboarding-plan-30-60-90 | Должность и приоритеты роли | [→](skills/hiring-and-hr/onboarding-plan-30-60-90/) | Создаёт адресный план адаптации нового сотрудника на 30-60-90 дней со стороны руководителя — цели, ключевые контакты, учебные вехи и критерии успеха на каждую фазу. Без HR-инструментов. Двуязычный EN/RU |
| interview-debrief-synthesizer | Заметки нескольких интервьюеров | [→](skills/hiring-and-hr/interview-debrief-synthesizer/) | Сводит разнородные заметки нескольких интервьюеров в один сравнимый разбор — свидетельства отделены от впечатлений с указанием источника, показаны расхождения между интервьюерами и непроверенные компетенции. Без ATS. Двуязычный EN/RU |

---

### III. Продукт

#### Discovery и UX-исследования

| Скилл | Input | Ссылка | Описание |
| ----- | ----- | ------ | -------- |
| user-feedback-synthesizer | Папка с файлами фидбека (.md/.txt/.csv) | [→](skills/discovery-and-user-research/user-feedback-synthesizer/) | Синтезирует транскрипты пользовательских интервью и feedback-файлы (.md, .txt, .csv) в приоритизированный инсайт-отчёт с темами, цитатами и открытыми вопросами. Двуязычный EN/RU |
| user-persona-synthesizer | Транскрипты интервью (текст или .md) | [→](skills/discovery-and-user-research/user-persona-synthesizer/) | Извлекает повторяющиеся пользовательские профили из реальных транскриптов CustDev-интервью и генерирует структурированные карточки персон с дословными цитатами и количеством респондентов. Двуязычный EN/RU |
| jobs-to-be-done-extractor | Папка с custdev-заметками (.md/.txt) | [→](skills/discovery-and-user-research/jobs-to-be-done-extractor/) | Извлекает JTBD-утверждения из папки с custdev-транскриптами и заметками интервью — ранжированная карта с цитатами, частотным анализом и паттернами. Двуязычный EN/RU |

#### Запуски и релизы

| Скилл | Input | Ссылка | Описание |
| ----- | ----- | ------ | -------- |
| prd-review-challenger | Текст PRD или файл | [→](skills/launch-and-releases/prd-review-challenger/) | Адвокат дьявола для PRD, фича-спецификаций и продуктовых решений — находит слабые допущения, открытые вопросы, риски реализации и логические дыры до того, как документ уйдёт в команду. Двуязычный EN/RU |
| release-notes-generator | Файл с итогами спринта (.md/.txt) | [→](skills/launch-and-releases/release-notes-generator/) | Преобразует plain-language итоги спринта в 4 формата user-facing release notes: changelog-запись, email-анонс, in-app push-уведомление и пост для соцсети. Git не нужен. Двуязычный EN/RU |
| feature-announcement-writer | Описание одной фичи (текст/.md) | [→](skills/launch-and-releases/feature-announcement-writer/) | Генерирует пакет анонса фичи в 4 форматах (changelog, email, push-уведомление, пост для соцсети) из одного описания продукта — без навыков копирайтинга. Двуязычный EN/RU |
| changelog-narrator | Две версии документа (.md/.txt) | [→](skills/launch-and-releases/changelog-narrator/) | Сравнивает две версии бизнес-документа и формирует читаемый changelog — без git и Track Changes. Работает с PRD, SOP, договорами и стратегическими документами. Двуязычный EN/RU |
| survey-results-analyzer | CSV-файл с результатами опроса | [→](skills/launch-and-releases/survey-results-analyzer/) | Анализирует CSV-экспорты опросов — частоты закрытых вопросов, темы открытых ответов и топ-3 инсайта без кода. Двуязычный EN/RU |

---

### IV. Данные

#### Анализ данных

| Скилл | Input | Ссылка | Описание |
| ----- | ----- | ------ | -------- |
| csv-data-analyzer | CSV-файл в рабочей папке | [→](skills/data-analysis/csv-data-analyzer/) | Анализирует CSV-файлы с бизнес-данными через диалоговый сценарий — без кода, без Python, без интеграций. Двуязычный EN/RU |
| report-analyzer | Файл отчёта PDF или PPTX | [→](skills/data-analysis/report-analyzer/) | Анализирует большие отчёты (PDF/PPTX) и формирует структурированное резюме с ключевыми данными и инсайтами |
| retention-cohort-interpreter | Вставленная таблица когорт удержания | [→](skills/data-analysis/retention-cohort-interpreter/) | Интерпретирует таблицу когортного удержания в диагноз: здоровье кривой, точки отвала, сравнение с бенчмарками, гипотезы и следующие шаги. Без аналитических инструментов. Двуязычный EN/RU |
| experiment-results-interpreter | Вставленные результаты A/B-теста | [→](skills/data-analysis/experiment-results-interpreter/) | Превращает результаты A/B теста в решение «шипать / откатить / продлить» — оценка статистической значимости в понятных словах, рекомендация с обоснованием и готовый текст для стейкхолдеров. Двуязычный EN/RU |
| metrics-anomaly-investigator | Описание аномалии метрики | [→](skills/data-analysis/metrics-anomaly-investigator/) | Преобразует описание метрической аномалии в ранжированный фреймворк гипотез и нарратив для стейкхолдеров — без базы данных и кода. Двуязычный EN/RU |

#### Метрики и отчёты для руководства

| Скилл | Input | Ссылка | Описание |
| ----- | ----- | ------ | -------- |
| kpi-digest-builder | Локальные файлы KPI (.md/.txt/.csv) | [→](skills/metrics-and-exec-narratives/kpi-digest-builder/) | Агрегирует числовые KPI из локальных файлов (.md, .txt, .csv) в еженедельный снапшот с дельтой к прошлой неделе — без кода и интеграций. Двуязычный EN/RU |
| exec-metrics-storyteller | Срез метрик и бизнес-контекст | [→](skills/metrics-and-exec-narratives/exec-metrics-storyteller/) | Превращает снапшот метрик в executive-отчёт для C-suite и борда с привязкой к revenue и LTV. Двуязычный EN/RU |
| weekly-metrics-story-writer | Вставленные недельные метрики и контекст | [→](skills/metrics-and-exec-narratives/weekly-metrics-story-writer/) | Преобразует числа дашборда в готовый еженедельный нарратив для стейкхолдеров — email или Slack, за несколько минут. Двуязычный EN/RU |
| north-star-metric-auditor | Текущая NSM и бизнес-модель | [→](skills/metrics-and-exec-narratives/north-star-metric-auditor/) | Оценивает North Star Metric по 4 критериям и предлагает 2–3 альтернативных кандидата с привязкой к бизнес-модели. Двуязычный EN/RU |

---

### V. Бизнес

#### Конкуренты и рынок

| Скилл | Input | Ссылка | Описание |
| ----- | ----- | ------ | -------- |
| competitive-feature-matrix-builder | Папка заметок о конкурентах (md/txt) | [→](skills/market-and-competitive-intelligence/competitive-feature-matrix-builder/) | Строит сравнительную feature matrix и gap-анализ из папки с конкурентными заметками (md/txt) — полностью офлайн, без веб-доступа. Двуязычный EN/RU |
| weekly-competitor-tracker | Папка competitors/ с .md-файлами | [→](skills/market-and-competitive-intelligence/weekly-competitor-tracker/) | Отслеживает еженедельные изменения конкурентов из markdown-заметок — сравнивает текущие файлы со снапшотом прошлой недели и формирует дельта-отчёт с оценкой значимости. Без API. Двуязычный EN/RU |
| industry-trend-brief | Папка статей (md/txt) | [→](skills/market-and-competitive-intelligence/industry-trend-brief/) | Синтезирует папку статей и вырезок в еженедельный тренд-бриф для продуктовой команды — ранжированные темы, сигналы с источниками и выводы. Полностью офлайн. Двуязычный EN/RU |

#### Маркетинг и контент

| Скилл | Input | Ссылка | Описание |
| ----- | ----- | ------ | -------- |
| campaign-retrospective-writer | Вставленные метрики и заметки кампании | [→](skills/marketing-and-content/campaign-retrospective-writer/) | Составляет структурированное ретро маркетинговой кампании из вставленных данных: цель vs. факт, разбор по каналам, что сработало/нет, рекомендации и строка тренда. Двуязычный EN/RU |
| content-performance-reporter | CSV-выгрузки аналитики платформ | [→](skills/marketing-and-content/content-performance-reporter/) | Компилирует CSV-экспорты аналитики контент-платформ (YouTube, GA4, LinkedIn и другие) в нарративный отчёт: что сработало, что нет, паттерн недели и рекомендации. Двуязычный EN/RU |
| research-to-content-brief | Папка исследовательских заметок (md/txt) | [→](skills/marketing-and-content/research-to-content-brief/) | Преобразует папку с research-заметками (аудитория, конкурентные сигналы, тренды) в структурированный контент-бриф из шести разделов. Без интервью. Двуязычный EN/RU |

#### Business Ops

| Скилл | Input | Ссылка | Описание |
| ----- | ----- | ------ | -------- |
| proposal-and-quote-drafter | Вставленные заметки со звонка | [→](skills/business-ops/proposal-and-quote-drafter/) | Превращает заметки со звонка в готовое КП: скоуп, три ценовых пакета, сопроводительное письмо и чеклист проверки. Двуязычный EN/RU |
| win-loss-debrief-writer | Вставленные заметки по сделке | [→](skills/business-ops/win-loss-debrief-writer/) | Генерирует структурированный win/loss-разбор из заметок по закрытой сделке: факторы решения, возражения, конкурентный контекст, что повторить / исправить, строка тренда для журнала сделок. CRM не нужен. Двуязычный EN/RU |
| fundraise-pipeline-tracker | Вставленные заметки по инвесторам | [→](skills/business-ops/fundraise-pipeline-tracker/) | Собирает структурированную воронку инвесторов из вставленных заметок: тиеринг Tier 1/2/3, статус по инвестору и приоритеты follow-up — без CRM. Двуязычный EN/RU |
| data-room-prep-checklist | Стадия раунда и бизнес-модель | [→](skills/business-ops/data-room-prep-checklist/) | По стадии раунда и бизнес-модели формирует приоритизированный чек-лист due diligence, структуру папок для data room и список пробелов с предсказуемыми вопросами инвестора. Без SaaS и интеграций. Двуязычный EN/RU |
| legal-matter-tracker | Имя клиента или дела | [→](skills/business-ops/legal-matter-tracker/) | Сканирует файлы воркспейса по имени клиента или названию дела и строит хронологию событий с ключевыми фактами — без интеграций. Двуязычный EN/RU |
| company-policy-drafter | Тип политики и параметры | [→](skills/business-ops/company-policy-drafter/) | Составляет или обновляет одну корпоративную политику (PTO, удалённая работа, расходы, AI-usage) для SMB-команд без штатного HR или юриста. Обязательный флаг юридической проверки. Двуязычный EN/RU |

#### Финансы и счета

| Скилл | Input | Ссылка | Описание |
| ----- | ----- | ------ | -------- |
| invoice-and-payment-tracker-summary | Вставленный список счетов | [→](skills/finance-and-billing/invoice-and-payment-tracker-summary/) | Из вставленного списка счетов формирует aging-сводку, акт сверки по клиентам и список «требует внимания» — без бухгалтерского SaaS и интеграций. Двуязычный EN/RU |
| accounts-receivable-followup-writer | Данные счёта и контекст отношений | [→](skills/finance-and-billing/accounts-receivable-followup-writer/) | Составляет эскалирующую серию из 4 напоминаний об оплате счёта (мягкое → финальное) по реквизитам счёта и контексту отношений с клиентом — с сохранением деловых отношений. Бухгалтерский SaaS не нужен. Двуязычный EN/RU |
| monthly-close-checklist-and-reconciliation-prep | Вставленный список транзакций (CSV/таблица) | [→](skills/finance-and-billing/monthly-close-checklist-and-reconciliation-prep/) | Превращает вставленную банковскую выгрузку или список транзакций в чек-лист месячного закрытия, черновик категоризации с флагами спорных транзакций и резюме для бухгалтера/инвестора — без SaaS и интеграций. Двуязычный EN/RU |

---

### VI. Личное и Claude

#### Личная продуктивность

| Скилл | Input | Ссылка | Описание |
| ----- | ----- | ------ | -------- |
| reading-list-prioritizer | .md-файл со списком чтения | [→](skills/personal-productivity/reading-list-prioritizer/) | Расставляет приоритеты и группирует md-список чтения по темам и релевантности роли — формирует недельный план чтения с шортлистом. Двуязычный EN/RU |
| newsletter-digest-builder | Папка со статьями .txt/.md | [→](skills/personal-productivity/newsletter-digest-builder/) | Преобразует папку с сохранёнными рассылками и статьями в структурированный еженедельный дайджест с приоритизацией по роли — группировка по темам, шортлист «Читать на этой неделе». Без интеграций. Двуязычный EN/RU |
| research-folder-synthesizer | Папка с файлами .md/.txt | [→](skills/personal-productivity/research-folder-synthesizer/) | Синтезирует папку смешанных файлов в структурированный тематический отчёт с темами, ключевыми находками и пробелами. Двуязычный EN/RU |
| workspace-health-monitor | Файлы воркспейса или вставленный текст | [→](skills/personal-productivity/workspace-health-monitor/) | Аудит рабочего пространства менеджера: находит осиротевшие файлы, забытые задачи, дубликаты и расхождения планов с реальностью. Двуязычный EN/RU |
| daily-admin-brief | Вставленные календарь, почта, задачи | [→](skills/personal-productivity/daily-admin-brief/) | Сводит вставленный дамп календаря, короткий список писем и открытые задачи в одностраничный бриф на день: главное, конфликты расписания, черновики ответов, даты для календаря. Без коннекторов. Двуязычный EN/RU |

#### Промпты и память

| Скилл | Input | Ссылка | Описание |
| ----- | ----- | ------ | -------- |
| prompt-builder | Ответы на вопросы | [→](skills/prompts-and-memory/prompt-builder/) | Создаёт структурированный промпт для любой задачи через серию вопросов |
| prompt-library-curator | Вставленные промпты или .md/.txt | [→](skills/prompts-and-memory/prompt-library-curator/) | Структурирует и тегирует личную коллекцию промптов в организованный markdown-каталог с индексной таблицей и определением дублей. Двуязычный EN/RU |
| memory-auditor-chat | Слои памяти текущей сессии | [→](skills/prompts-and-memory/memory-auditor-chat/) | Аудит и очистка нативной памяти Claude.ai: находит противоречия, устаревшие записи, дубли и шум в Memory Edits и Memory Summary. Двуязычный EN/RU |
| memory-auditor-cowork | Файлы памяти воркспейса Cowork | [→](skills/prompts-and-memory/memory-auditor-cowork/) | Аудит и очистка файловой памяти в Cowork: auto-memory, CLAUDE.md, User Preferences и Project Instructions. Двуязычный EN/RU |

#### Сессии и контекст

| Скилл | Input | Ссылка | Описание |
| ----- | ----- | ------ | -------- |
| session-handoff-composer | Текущая сессия | [→](skills/sessions-and-context/session-handoff-composer/) | Составляет структурированный handoff-блок из текущей сессии при переполнении контекста — решения, задачи, открытые вопросы и следующие шаги, готовые к вставке в новую сессию. Двуязычный EN/RU |
| context-window-health-check | Текущая сессия | [→](skills/sessions-and-context/context-window-health-check/) | Оценивает состояние текущей сессии Claude и даёт понятный статус (🟢/🟡/🔴) с одной конкретной рекомендацией: продолжать, сделать handoff или начать новую сессию. Без технических метрик. Двуязычный EN/RU |
| cowork-session-planner | Текущая папка проекта | [→](skills/sessions-and-context/cowork-session-planner/) | Генерирует пре-сессионный бриф для Cowork по файлам проекта — текущий статус, цель сессии и приоритизированный план работы до первого сообщения. Двуязычный EN/RU |

#### Настройка и аудит

| Скилл | Input | Ссылка | Описание |
| ----- | ----- | ------ | -------- |
| feature-guide | Название фичи или описание задачи | [→](skills/setup-and-audit/feature-guide/) | Мгновенно объясняет любую возможность Claude: что это, где доступна, какой тариф нужен, как активировать, ограничения и вердикт о применимости. Двуязычный EN/RU |
| cowork-plugin-audit | Список плагинов и описание работы | [→](skills/setup-and-audit/cowork-plugin-audit/) | Аудит установленных плагинов Cowork в контексте workflow — таблица рекомендаций оставить/отключить с оценкой снижения токен-расхода. Без интеграций. Двуязычный EN/RU |
| skill-usage-log-reviewer | Вставленный список установленных скилов | [→](skills/setup-and-audit/skill-usage-log-reviewer/) | Аудит коллекции установленных скилов Claude — выявляет неиспользуемые, находит дубликаты, генерирует чеклист деактивации для снижения шума в контексте. Двуязычный EN/RU |
| routines-setup-assistant | Ответы на вопросы | [→](skills/setup-and-audit/routines-setup-assistant/) | Настраивает Scheduled Tasks в Claude Cowork через интервью — генерирует готовые к вставке промпты для автоматизации повторяющихся задач. Без интеграций. Двуязычный EN/RU |
| weekly-ai-workflow-review | .md-файл или вставленный лог задач | [→](skills/setup-and-audit/weekly-ai-workflow-review/) | Анализирует еженедельные заметки о задачах, делегированных Claude: паттерны делегирования, удачные промпты, точки оптимизации и шаблоны промптов. Двуязычный EN/RU |
| setup-wizard | Ссылка на сервис и цель настройки | [→](skills/setup-and-audit/setup-wizard/) | Ведёт по настройке внешнего сервиса или IT-инструмента шаг за шагом — строит маршрут по официальной справке и закрывает шаг только по присланному доказательству. Команды за вас не выполняет. Двуязычный EN/RU |

---

## Как установить скилл

### Вариант 1 — Git clone (весь набор)

```bash
git clone https://github.com/KirKruglov/claude-skills-kit.git
```

Нужная папка скилла будет по пути `skills/<group>/<skill-name>/`.

Другие варианты установки (sparse-checkout, скачивание одного скилла и т.д.) — в [INSTALL.ru.md](INSTALL.ru.md).

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

См. [CONTRIBUTING.md](CONTRIBUTING.md) — как предложить скилл, сообщить о проблеме или улучшить документацию.

---

## Community

| Файл | Назначение |
| ---- | ---------- |
| [CONTRIBUTING.md](CONTRIBUTING.md) | Как предложить скилл, сообщить об ошибке, улучшить документацию |
| [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) | Стандарты сообщества |
| [SECURITY.md](SECURITY.md) | Как сообщить о проблеме безопасности |
| [GitHub Discussions](https://github.com/KirKruglov/claude-skills-kit/discussions) | Вопросы, идеи, общение |

Шаблоны issues и PR активны автоматически через `.github/`.

---

## Лицензия

MIT
