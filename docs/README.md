# Документация — Credit Journey

## О кейсе

Проект про онлайн-выдачу займа: на критическом пути решения встроена проверка кредитной истории в бюро кредитных историй (**[БКИ](glossary/terms.md#bki)**), а на шаге выдачи — [оффер](glossary/terms.md#offer) страхования (**[opt-in](glossary/terms.md#opt-in)**: отказ от полиса не блокирует займ).

Сейчас проверка [КИ](glossary/terms.md#ki) и страхование часто разрознены или появляются слишком поздно в процессе. Из‑за этого растут [Time-to-Decision](glossary/terms.md#time-to-decision) и [Time-to-Cash](glossary/terms.md#time-to-cash), страдает конверсия воронки и недобирается доход от страхового кросс-селла — при том что качество риска сложно контролировать единообразно.

Цель кейса — собрать единый цифровой [journey](glossary/terms.md#journey) без роста ранней просрочки сверх согласованного порога.

Цепочка целевого процесса (**[TO-BE](glossary/terms.md#to-be)**): заявка → согласия ([ПДн](glossary/terms.md#pdn) + БКИ) → проверка БКИ → решение ([approve / decline](glossary/terms.md#approve-decline) / [manual review](glossary/terms.md#manual-review)) → оффер займа → оффер страховки (opt-in) → выдача.

Горизонт: **8–12 недель**, два релиза (**[MVP](glossary/terms.md#mvp) → [Phase 2](glossary/terms.md#phase-2)**). [KPI](glossary/terms.md#kpi), [scope](glossary/terms.md#scope) и out of scope — в [one-pager](one-pager.md). Незнакомые термины — в [глоссарии](glossary/terms.md).

## Артефакты

| Документ | Путь | Статус |
|----------|------|--------|
| One-pager | [one-pager.md](one-pager.md) | Согласовано (v1.0) |
| Стейкхолдеры и RACI | [stakeholders-raci.md](stakeholders-raci.md) | Согласовано (v1.0) |
| AS-IS процесс | [processes/as-is-loan-process.md](processes/as-is-loan-process.md) | Согласовано (v1.0) |
| TO-BE journey | [processes/to-be-loan-journey.md](processes/to-be-loan-journey.md) | Согласовано (v1.0) |
| BRD | [brd/brd-credit-journey.md](brd/brd-credit-journey.md) | Рамка v1.0 согласована (часть входов — Ожидает данных) |
| Open points | [brd/open-points.md](brd/open-points.md) | Лог Q1–Q7 (ведение TBD) |
| План MVP | [plan/mvp-schedule.md](plan/mvp-schedule.md) · [plan/gantt-mvp.png](plan/gantt-mvp.png) | v1.1: вехи, волны, скрин Ганта (MS Project B) |
| Backlog / эпики | [backlog/jira-epics-mvp.md](backlog/jira-epics-mvp.md) | Согласовано (v1.0) |
| Риски | [risks/risk-register.md](risks/risk-register.md) | Согласовано (v1.0) |
| Коммуникации | [communications/communication-plan.md](communications/communication-plan.md) | Согласовано (v1.0) |
| Глоссарий | [glossary/terms.md](glossary/terms.md) | Согласовано (v1.0) |
