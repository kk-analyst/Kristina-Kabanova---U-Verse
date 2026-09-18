# Оплата курсов

## Бизнес-контекст

Студент покупает курс и при оформлении заказа может применить промокод. Оплата выполняется через внешнего платёжного провайдера. 

## Основной сценарий

```text
Student
  ↓
Frontend
  ↓
Backend
  ↓
DB + payment provider
  ↓
External payment form
  ↓
Webhook
  ↓
Backend validation
  ↓
DB status update
  ↓
Frontend status request
```

## Ключевые проектные решения

### Frontend не устанавливает статус платежа PAID

Возврат по successUrl/failUrl не считается подтверждением оплаты.

### Webhook валидируется

Проверяются структура, обязательные параметры, подпись, существование платежа, внешний ID и сумма.

### Статус читается из U-Verse

После возврата пользователя Frontend получает актуальный статус через Backend; синхронный запрос к провайдеру для каждого чтения не выполняется.

## Статусная модель

- CREATED
- WAITING_FOR_PAYMENT
- PAID
- CANCELED

## Ошибки

Проработаны сценарии 403, 500, 502, 504 и некорректного webhook.

## Артефакты

- [API](../docs/api.md)
- [Integrations](../docs/integrations.md)
- [Use Cases](../docs/use-cases.md)
- [Testing & Errors](../docs/testing-and-errors.md)
- [Diagrams](../docs/diagrams.md)
