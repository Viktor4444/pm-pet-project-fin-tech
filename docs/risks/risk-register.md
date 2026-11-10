# Реестр рисков — Credit Journey MVP

> Термины: [MVP](../glossary/terms.md#mvp) · [KPI](../glossary/terms.md#kpi) · [epic](../glossary/terms.md#epic)

**Версия:** 1.0  
**Дата:** 2026-11-09  
**Согласовано:** Продуктовый отдел (бизнес-заказчик) при участии IT-отдела, Отдела кредитных рисков, Комплаенс и юридического отдела, Операционного отдела и Отдела QA (подтверждение реестра и владельцев митигаций)  
**Подготовил:** PM / BA  

**Опора:** [One-pager](../one-pager.md) §8, [BRD](../brd/brd-credit-journey.md), [TO-BE](../processes/to-be-loan-journey.md), [Эпики Jira](../backlog/jira-epics-mvp.md)  
**Владелец реестра:** PM / BA (фасилитация); владельцы митигаций — по строкам.

---

## 1. Шкала

| Уровень | Вероятность (P) | Влияние (I) |
|---------|-----------------|-------------|
| L (1) | маловероятно на горизонте [MVP](../glossary/terms.md#mvp) | локальный сдвиг / лёгкий дискомфорт [KPI](../glossary/terms.md#kpi) |
| M (2) | реально возможно | заметный сдвиг срока или KPI |
| H (3) | ожидаемо без митигации | срыв MVP / compliance / сильный удар по KPI |

**Балл** = P × I (1–9). Фокус управления: балл ≥ 6, плюс любые compliance-риски с I=H.

Статусы риска: `open` · `mitigating` · `accepted` · `closed`.

---

## 2. Реестр

| ID | Риск | Категория | P | I | Балл | Владелец | Митигация | Ранний сигнал | BRD / Q | Статус |
|----|------|-----------|---|---|------|----------|-----------|---------------|---------|--------|
| R01 | Нестабильный / медленный [SLA](../glossary/terms.md#sla) [БКИ](../glossary/terms.md#bki) → рост TTD, очередь MR | партнёр / техника | H | H | 9 | IT-отдел | таймауты, ретраи, fallback в MR (без approve без актуального ответа БКИ); мониторинг p95 (E2, E7) | рост latency/error rate; рост `MR_BKI_*` | Q2 | mitigating |
| R02 | Срыв согласования согласий / отказных текстов (Комплаенс) | compliance | M | H | 6 | Комплаенс и юридический отдел | раннее ревью до freeze [scope](../glossary/terms.md#scope); BR-02…04 в E1 | затянутый review текстов > `[TBD]` дней | Q4 | open |
| R03 | Scope creep (ML-скоринг, своё МП, «ещё одна» интеграция) | scope | M | H | 6 | Продуктовый отдел | жёсткий out of scope; change control через [RACI](../glossary/terms.md#raci) | запросы вне BRD без Epic | — | open |
| R04 | Низкий [take-rate](../glossary/terms.md#take-rate) страховки при выдаче | продукт | M | M | 4 | Продуктовый отдел | [оффер](../glossary/terms.md#offer) на шаге выдачи ([opt-in](../glossary/terms.md#opt-in)); понятная ценность; тексты с Комплаенс (E6) | низкий `insurance_offer_accepted` на пилоте | Q4 | open |
| R05 | Расхождение данных [АБС](../glossary/terms.md#abs) ↔ БКИ / страховой партнёр | техника | M | H | 6 | IT-отдел | контракт полей; идемпотентность выдачи/полиса; сверки статусов | ручные правки после выдачи; дубли | Q5 | open |
| R06 | Перегруз очереди [manual review](../glossary/terms.md#manual-review) | операции / риск | M | H | 6 | Отдел кредитных рисков + Операционный отдел | правила → MR только по критериям; БКИ вовремя; целевой % MR `[TBD]` (E3, E4) | рост share MR; SLA разбора очереди | Q3 | open |
| R07 | Сбой страхового API на шаге выдачи | партнёр / техника | M | M | 4 | IT-отдел | BR-34: выдача без оффера + инцидент (E6, E7) | error rate партнёра; `skipped_unavailable` | — | mitigating |
| R08 | Approve без актуальной [КИ](../glossary/terms.md#ki) при деградации БКИ (обход процесса) | риск / compliance | L | H | 3 | Отдел кредитных рисков | запрет в BRD/TO-BE; только MR после ретраев | попытки hotfix без MR | — | open |
| R09 | Открытые [`TBD`](../glossary/terms.md#tbd) (SLA, тексты, % MR, поля полиса) блокируют разработку | поставка | H | M | 6 | PM / BA | лог [open points](../brd/open-points.md) (Q1–Q7); владельцы ответов; привязка к вехам — после `docs/plan/` | Epic без [DoR](../glossary/terms.md#dor-dod) из‑за TBD | Q1–Q7 | open |
| R10 | Неготовность к [UAT](../glossary/terms.md#uat) / критичные дефекты на gate | качество | M | H | 6 | Отдел QA | чек-листы E8 с середины волны; UAT-сценарии из BRD | красный регресс на ключевых сценариях | — | open |
| R11 | Конфликт «скорость релиза vs risk/compliance» | scope / орг. | M | H | 6 | PM / BA | эскалация на совместный созвон Product + Риски + Комплаенс | параллельные «срочные» исключения из правил | — | open |
| R12 | Сбой зачисления / неясная политика ретраев выдачи | техника | M | M | 4 | IT-отдел | статус ошибки клиенту; политика `[TBD]` → следующая версия BRD / [Phase 2](../glossary/terms.md#phase-2) | рост failed disbursement | Q6 | open |

---

## 3. Приоритет внимания (балл ≥ 6)

1. **R01** SLA БКИ  
2. **R02** Compliance-тексты  
3. **R03** Scope creep  
4. **R05** Рассинхрон данных  
5. **R06** Очередь MR  
6. **R09** Блокирующие TBD  
7. **R10** UAT gate  
8. **R11** Скорость vs controls  

R04/R07/R12 — мониторить; R08 — низкая вероятность при дисциплине процесса, высокий ущерб → контроль через DoD/ревью.

---

## 4. Связь с эпиками

| Риск | Эпики | Jira Suggested name |
|------|-------|---------------------|
| R01, R08 | E2, E3, E4, E7 | `CJ: Credit Bureau Integration`, `CJ: Decision Rules Engine`, `CJ: Manual Review Queue`, `CJ: Integration Monitoring` |
| R02 | E1 | `CJ: Application & Consents` |
| R03, R11 | change control / все | — |
| R04, R07 | E6, E7 | `CJ: Insurance Opt-in Offer`, `CJ: Integration Monitoring` |
| R05, R12 | E5, E6 | `CJ: Loan Offer & Disbursement`, `CJ: Insurance Opt-in Offer` |
| R06 | E3, E4 | `CJ: Decision Rules Engine`, `CJ: Manual Review Queue` |
| R09 | все (DoR) | см. [эпики](../backlog/jira-epics-mvp.md) |
| R10 | E8 | `CJ: UAT & MVP Quality Gate` |

---

## 5. Ритуал

- Обзор реестра на статус-встрече (см. [план коммуникаций](../communications/README.md)): новые риски, изменение балла, снятие `closed`.
- Эскалация балла ≥ 6 без митигации > 1 цикл статуса → Продуктовый отдел (+ профильный Accountable).
