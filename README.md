# Credit Journey

Пет-проект кейс для портфолио **Product / BA / PM** в потребительском кредитовании (онлайн-займ в логике МФО).

## Проблема

Проверка кредитной истории и предложение страхования разрознены или происходят слишком поздно в journey выдачи. Из‑за этого растут Time-to-Decision и Time-to-Cash, падает конверсия воронки и недобирается доход от страхового кросс-селла — при этом качество риска сложно контролировать.

## Цель

Собрать единый цифровой journey: заявка → согласия → проверка БКИ → решение → оффер займа → оффер страхования (opt-in) → выдача — без роста ранней просрочки сверх согласованного порога.

## Горизонт кейса

- **8–12 недель**, два релиза: **MVP → Phase 2**
- Демонстрируемые роли: Product + Business Analysis + Project Management (совмещённо)

## MVP (Release 1) кратко

- Цифровая заявка на займ
- Явные согласия (ПДн + запрос в БКИ)
- Интеграция с БКИ на критическом пути решения
- Решение: approve / decline / manual review
- Оффер страхования на шаге выдачи (opt-in)
- Базовый мониторинг интеграций и UAT

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

Документы публикуются по мере согласования. В финальном виде: [one-pager](docs/one-pager.md), [стейкхолдеры и RACI](docs/stakeholders-raci.md), [AS-IS](docs/processes/as-is-loan-process.md), [TO-BE](docs/processes/to-be-loan-journey.md), [BRD](docs/brd/brd-credit-journey.md). Остальное — по мере ревью.

## Статус

**Опубликованы:** one-pager, RACI, AS-IS, TO-BE, BRD (v1.0; у BRD часть входов — «Ожидает данных»). Далее: backlog, риски, коммуникации.
