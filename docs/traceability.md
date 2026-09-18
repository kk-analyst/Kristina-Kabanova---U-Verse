# Traceability Matrix

Матрица показывает связь между требованиями и техническими артефактами.

| Requirement | Use Case | API / Integration | Business Rule | Data |
|---|---|---|---|---|
| FR-001 Баланс баллов | Loyalty balance | Loyalty API | BR-001 | Bonus account |
| FR-002 История баллов | Loyalty history | Loyalty API | BR-005/006 | Bonus operation |
| FR-003 Frontend не меняет PAID | UC-1 | Payment webhook | BR-007/008 | Payment |
| FR-004 Статус из Backend | UC-1 | Payment status API | BR-007 | Payment |
| FR-005 Проверка ADMIN | UC-2/3 | Applications API | BR-010 | User/Application |
| FR-006 Фильтрация заявок | UC-2 | GET applications | — | Application |

Матрица намеренно ограничена требованиями, которые можно связать с конкретными материалами проектного кейса.
