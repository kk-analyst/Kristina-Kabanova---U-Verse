# Integration: RaifPay

## Purpose

Проведение оплаты через внешнюю платёжную форму.

## Participants

- Student
- U-Verse Frontend
- U-Verse Backend
- RaifPay
- U-Verse DB

## Protocol

HTTPS / REST API + webhook.

## Authentication

Способ аутентификации и формат подписи webhook должны соответствовать договорённости/документации конкретного провайдера. В проектном сценарии Backend выполняет проверку подписи webhook.

## Sequence

```text
Student → Frontend: start payment
Frontend → Backend: create payment
Backend → RaifPay: create payment
RaifPay → Frontend: external payment form
RaifPay → Backend: webhook
Backend → DB: validate + update
Frontend → Backend: GET payment status
Backend → Frontend: current status
```

## Important decision

successUrl/failUrl не используются как доказательство факта оплаты.

Факт изменения статуса определяется Backend после обработки webhook.

## Amount validation

Сумма из webhook сопоставляется с суммой платежа, сохранённой в U-Verse.

## Retry / delivery

Webhook должен корректно обрабатываться при повторной доставке. После принятия корректного сообщения Backend возвращает HTTP 200.

В проектном сценарии предусмотрено, что провайдер может повторять доставку в течение длительного периода (до 24 часов).

## Data boundary

U-Verse не принимает и не хранит карточные данные при использовании внешней платёжной формы.
