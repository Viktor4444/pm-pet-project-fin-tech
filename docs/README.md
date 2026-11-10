# Документация — Credit Journey

## О кейсе

Проект про онлайн-выдачу займа: на критическом пути решения встроена проверка кредитной истории в бюро кредитных историй (**БКИ**), а на шаге выдачи — оффер страхования (**opt-in**: отказ от полиса не блокирует займ).

Сейчас проверка КИ и страхование часто разрознены или появляются слишком поздно в процессе. Из‑за этого растут Time-to-Decision и Time-to-Cash, страдает конверсия воронки и недобирается доход от страхового кросс-селла — при том что качество риска сложно контролировать единообразно.

Цель кейса — собрать единый цифровой journey без роста ранней просрочки сверх согласованного порога.

Цепочка целевого процесса (**TO-BE**): заявка → согласия (ПДн + БКИ) → проверка БКИ → решение (approve / decline / manual review) → оффер займа → оффер страховки (opt-in) → выдача.

Горизонт: **8–12 недель**, два релиза (**MVP → Phase 2**). KPI, scope и out of scope — в [one-pager](one-pager.md). Незнакомые термины — в [глоссарии](glossary/terms.md).

## Артефакты

| Документ | Путь | Статус |
|----------|------|--------|
| One-pager | [one-pager.md](one-pager.md) | Согласовано (v1.0) |
| Стейкхолдеры и RACI | [stakeholders-raci.md](stakeholders-raci.md) | Согласовано (v1.0) |
| AS-IS процесс | [processes/as-is-loan-process.md](processes/as-is-loan-process.md) | Согласовано (v1.0) |
| TO-BE journey | [processes/to-be-loan-journey.md](processes/to-be-loan-journey.md) | Согласовано (v1.0) |
| BRD | [brd/brd-credit-journey.md](brd/brd-credit-journey.md) | Рамка v1.0 согласована (часть входов — Ожидает данных) |
| Backlog / эпики | [backlog/jira-epics-mvp.md](backlog/jira-epics-mvp.md) | Согласовано (v1.0) |
| Риски | [risks/risk-register.md](risks/risk-register.md) | Согласовано (v1.0) |
| Коммуникации | [communications/communication-plan.md](communications/communication-plan.md) | Согласовано (v1.0) |
| Глоссарий | [glossary/terms.md](glossary/terms.md) | Согласовано (v1.0) |
