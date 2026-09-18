# API — Pruffme

## POST /api/v1/flows/{flowId}/webinars

Создание вебинара в рамках учебного потока.

### Authorization

Bearer Token. Операция доступна преподавателю.

### Request

Показательные поля контракта:

| Field | Description |
|---|---|
| title | название |
| shortDescription | краткое описание |
| description | описание |
| image | изображение |
| startAt | дата/время начала |
| durationMinutes | продолжительность |
| number | номер вебинара |

Для передачи контента внешнему API в проектном сценарии используется предусмотренный документацией формат, включая Base64 для соответствующих данных.

### Business rules

- вебинар создаётся в указанном flow;
- повторное создание при конфликте идентификаторов обрабатывается как конфликт;
- данные U-Verse преобразуются в формат Pruffme через mapping.

### Errors

| HTTP | Scenario |
|---|---|
| 404 | flow / webinar не найден |
| 409 | конфликт / дубликат |
| 502 | ошибка внешнего сервиса |

### Rate limit

В проектных материалах для данного API зафиксировано ограничение порядка **100 запросов в минуту**. Перед публикацией следует сверить значение с актуальной версией исходной документации Pruffme.

## Integration mapping

```text
U-Verse
  title            → Pruffme title
  shortDescription → Pruffme shortDescription
  description      → Pruffme description
  startAt          → Pruffme startAt
  durationMinutes  → Pruffme durationMinutes
  number           → Pruffme number
```
