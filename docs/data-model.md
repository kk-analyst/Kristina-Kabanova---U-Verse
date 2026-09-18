# Data Model

Модель данных в проектном кейсе используется как связующее звено между бизнес-правилами и API.

## Основные домены

### Payments

Показательные сущности:

- Order;
- Payment;
- Payment status history.

Ключевая связь: заказ хранит бизнес-контекст покупки, Payment — состояние платежной операции, history — последовательность изменений статуса.

### Loyalty

Показательные сущности:

- Bonus account;
- Bonus operation;
- Promo code.

Для операции важны тип операции, сумма баллов, основание, время операции и остаток после операции.

### Teacher Recruitment

Показательные данные заявки включают:

- идентификатор;
- ФИО;
- дату рождения;
- телефон;
- email;
- образование;
- опыт;
- дисциплину;
- статус;
- дату подачи;
- связанные документы;
- комментарии.

## Пример маппинга данных API → DB

| API field | Смысл | DB / domain |
|---|---|---|
| id | идентификатор заявки | application.id |
| lastName | фамилия | application.last_name |
| firstName | имя | application.first_name |
| middleName | отчество | application.middle_name |
| submittedAt | дата подачи | application.submitted_at |
| status | текущее состояние | application.status |
| email | email кандидата | application.email |

## Validation examples

| Поле | Тип | Требование |
|---|---|---|
| lastName | string | 2–50 символов, кириллица |
| firstName | string | 2–50 символов, кириллица |
| middleName | string/null | необязательное |
| birthDate | date | YYYY-MM-DD |
| phone | string | E.164 |
| email | string | RFC 5322 |
| discipline | enum | допустимое значение справочника |

Модель демонстрирует аналитическую проработку данных в проектном кейсе.
