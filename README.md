# Credit Journey

Интеграционный кейс выдачи онлайн-займа с проверкой БКИ и оффером страхования на шаге выдачи.

## Что это

Пет-проект на роль **менеджера проектов** (портфолио). Предмет кейса — финтех / потребительское кредитование (онлайн-займ в логике МФО).

## Зачем смотреть

- Предпроектное обследование и бизнес-требования (one-pager, BRD, RACI)
- Моделирование процессов: AS-IS и TO-BE journey
- Планирование и контроль исполнения (мастер-план MS Project и Jira — в roadmap)
- Управление рисками и коммуникации со стейкхолдерами
- Декомпозиция MVP в эпики backlog

## Горизонт кейса

**8–12 недель**, два релиза: **MVP → Phase 2**. Детали scope, KPI и требований — в `docs/`.

## Карта репозитория

| Путь | Что внутри |
|------|------------|
| [docs/one-pager.md](docs/one-pager.md) | One-pager: проблема, цели, KPI, scope |
| [docs/stakeholders-raci.md](docs/stakeholders-raci.md) | Стейкхолдеры и RACI |
| [docs/processes/](docs/processes/) | AS-IS процесс и TO-BE journey |
| [docs/brd/](docs/brd/) | Business Requirements Document |
| [docs/backlog/](docs/backlog/) | Эпики / контур backlog MVP |
| [docs/risks/](docs/risks/) | Реестр рисков |
| [docs/communications/](docs/communications/) | План коммуникаций |

Полный индекс: [docs/README.md](docs/README.md).

## Статус

Базовый пакет документов согласован и опубликован в `docs/` (v1.0).

## Roadmap доработок

Актуальный список того, что ещё появится в портфолио:

- Управление открытыми вопросами требований (open points)
- Мастер-план MVP (MS Project: вехи, скрин Ганта, CSV в `docs/plan/`)
- Jira: эпики `CJ: …` + симуляция исполнения (mirror в git)
- User stories на 1–2 эпика
- Связка план ↔ backlog ↔ риски
- UAT / go-live чек-лист
- Пример статус-отчёта
- (позже) MCP Jira; экспорт схем процессов

## Инструменты исполнения

| Инструмент | В репозитории |
|------------|---------------|
| **Документы** | уже в `docs/` |
| **MS Project** | появится в `docs/plan/` (вехи, скрин Ганта, CSV/XML) |
| **Jira** | эпики уже описаны в backlog; далее — проект, симуляция статусов, mirror stories |
| **Confluence** | роль в плане коммуникаций; контент кейса = git `docs/` |
| **MCP Jira** | позже, после живой Jira |

## Как читать

Жёсткого маршрута нет. Удобный вход:

1. Сначала эта **карта** и индекс [docs/README.md](docs/README.md) — общее понимание, что где лежит.
2. Затем, если хотите пройти кейс целиком, рекомендуемый порядок:  
   [one-pager](docs/one-pager.md) → [RACI](docs/stakeholders-raci.md) → [AS-IS](docs/processes/as-is-loan-process.md) / [TO-BE](docs/processes/to-be-loan-journey.md) → [BRD](docs/brd/brd-credit-journey.md) → [эпики](docs/backlog/jira-epics-mvp.md) → [риски](docs/risks/risk-register.md) → [коммуникации](docs/communications/communication-plan.md).
3. По интересу можно сразу: процессы → `docs/processes/`; требования → `docs/brd/`; backlog → `docs/backlog/`; риски → `docs/risks/`; коммуникации → `docs/communications/`.
