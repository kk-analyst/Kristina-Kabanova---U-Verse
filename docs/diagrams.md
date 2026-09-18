# Diagrams

Диаграммы используются для фиксации поведения системы и взаимодействия компонентов.

## Sequence: payment

```text
Student → Frontend: initiate payment
Frontend → Backend: create order/payment
Backend → DB: save payment
Backend → RaifPay: create payment
RaifPay → Backend: payment link / response
Backend → Frontend: payment link
Frontend → RaifPay: open form
RaifPay → Backend: webhook
Backend → DB: update status
Frontend → Backend: get payment status
Backend → Frontend: current status
```

## State: payment

```text
CREATED
   ↓ payment initiated
WAITING_FOR_PAYMENT
   ↓ webhook: success
PAID

WAITING_FOR_PAYMENT
   ↓ cancellation / failure
CANCELED
```

## Sequence: T-Bank registry

```text
Scheduler → U-Verse: form registry
Admin → U-Verse: confirm
U-Verse → T-Bank: create-submit
T-Bank → U-Verse: 202 + correlationId
U-Verse → T-Bank: polling GET
T-Bank → U-Verse: current status
U-Verse → DB: synchronize
```

## BPMN

Исходные проектные материалы содержат BPMN по процессам:

- найм преподавателя;
- оплата курса;
- регистрация/начисление в системе лояльности.

При добавлении исходников диаграмм их следует хранить в PlantUML/BPMN-формате рядом с визуализацией.
