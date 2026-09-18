# Integration: Pruffme

## Purpose

Создание вебинаров из U-Verse во внешней системе вебинаров.

## Participants

Teacher → U-Verse Backend → Pruffme

## Endpoint

`POST /api/v1/flows/{flowId}/webinars`

Authorization: Bearer Token.

## Data mapping

U-Verse преобразует данные вебинара в контракт Pruffme: title, shortDescription, description, image, startAt, durationMinutes, number.

Для соответствующих данных используется формат Base64.

## Conflict handling

Если внешний сервис сообщает о дубликате, U-Verse обрабатывает конфликт как `409`.

## External failures

Ошибка внешнего сервиса не должна маскироваться под успешное создание вебинара.

В проектной документации отдельно рассматриваются `404` для отсутствующей сущности и `502` для ошибки внешнего сервиса.

## Additional artifact

Для интеграции проработаны mapping и сценарии обработки ошибок.
