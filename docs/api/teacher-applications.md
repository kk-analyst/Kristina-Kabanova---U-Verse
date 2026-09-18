# API — Teacher Applications

## GET /api/v1/applications

Получение списка заявок преподавателей для административного интерфейса.

### Query parameters

| Parameter | Purpose |
|---|---|
| page | номер страницы |
| size | размер страницы |
| sort | поле/направление сортировки |

В проектном сценарии предусмотрена сортировка по ФИО и пагинация.

### Authorization

Операция доступна пользователю с ролью **ADMIN**.

### Errors

| HTTP | Meaning |
|---|---|
| 400 | некорректные параметры запроса |
| 401 | пользователь не авторизован |
| 403 | недостаточно прав |
| 503 | сервис временно недоступен |

## GET /api/v1/applications/{id}

Получение деталей конкретной заявки.

Данные заявки объединяются с информацией о прикреплённых документах из файлового хранилища.

## PATCH /api/v1/applications/{id}/status

Изменение статуса заявки.

### Request

```json
{
  "status": "IN_REVIEW"
}
```

Допустимые значения статуса:

- NEW
- IN_REVIEW
- INTERVIEW_INVITED
- REVISION_REQUIRED
- APPROVED
- REJECTED
- ARCHIVED

Конкретные разрешённые переходы определяются статусной моделью.

## POST /api/v1/applications

В проектном кейсе метод используется для операций с набором заявок при массовом изменении статуса.

> Контракт массовой операции следует сверять с исходной спецификацией перед публикацией: в разных версиях проектных материалов встречается различная форма bulk-запроса.

## Validation

| Field | Validation |
|---|---|
| lastName | 2–50 символов, кириллица |
| firstName | 2–50 символов, кириллица |
| middleName | nullable |
| birthDate | YYYY-MM-DD |
| email | до 254 символов, RFC 5322 |
| discipline | enum |
| education | enum |
| experience | enum |
| documents | PDF/JPG/JPEG/PNG/DOC/DOCX |

### Discipline enum

`PHYSICS`, `MATH`, `CHEMISTRY`, `FOREIGN_LANGUAGES`, `HUMANITIES`, `COMPUTER_SCIENCE`, `OTHER`.

Для `OTHER` требуется дополнительное описание дисциплины.

### Education enum

`SECONDARY_SPECIAL`, `BACHELOR`, `MASTER`, `SPECIALIST`, `PHD`.

### Experience enum

`ZERO_TO_ONE`, `TWO_TO_FIVE`, `SIX_TO_TEN`.

## Negative scenarios

- некорректные значения enum;
- отсутствует обязательное поле;
- email не проходит валидацию;
- заявка не найдена;
- пользователь не имеет роли ADMIN;
- недопустимый переход статуса;
- конфликт при массовой операции.
