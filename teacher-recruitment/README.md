# Teacher Recruitment

## Business context

Администратор работает с заявками кандидатов на преподавательские позиции: просматривает, фильтрует и обрабатывает заявки, меняет статусы и работает с документами.

## Main scenarios

- просмотр списка;
- фильтрация;
- просмотр деталей;
- добавление комментария;
- изменение статуса;
- массовая обработка;
- отправка уведомления кандидату.

## API

- `GET /api/v1/applications`
- `GET /api/v1/applications/{id}`
- `POST /api/v1/applications/{id}/comments`
- `PATCH /api/v1/applications/{id}/state`

## Status model

В проектных материалах проработан жизненный цикл заявки, включая состояния:

`NEW → IN_REVIEW → INTERVIEW_INVITED → REVISION_REQUIRED → APPROVED / REJECTED → ARCHIVED`

Конкретные допустимые переходы должны соответствовать таблице переходов в исходной документации.

## Validation

Показательные правила:

| Поле | Validation |
|---|---|
| Фамилия | 2–50 символов, кириллица |
| Имя | 2–50 символов, кириллица |
| Отчество | необязательное |
| Дата рождения | YYYY-MM-DD |
| Телефон | E.164 |
| Email | RFC 5322 |
| Дисциплина | значение справочника |

## Errors

Для списка заявок проработаны 400 / 401 / 403 / 503.

## Artifacts

- [Requirements](../docs/requirements.md)
- [API](../docs/api.md)
- [Use Cases](../docs/use-cases.md)
- [Data Model](../docs/data-model.md)
- [Testing & Errors](../docs/testing-and-errors.md)
