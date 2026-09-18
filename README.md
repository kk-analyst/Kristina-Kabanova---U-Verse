# Kristina Kabanova

## System Analyst · Junior / Junior+

Портфолио системного анализа на проекте **U-Verse** — облачной образовательной платформе для обучения взрослых.

Я прорабатываю требования и системные решения на стыке бизнес-логики и технической реализации: декомпозиция требований, API, интеграции, модели данных, UML/BPMN, валидация, ошибки и техническая документация.

> **Project status:** учебный проект / проектный кейс. Описанные решения — результаты проектирования и документирования, а не подтверждение промышленной эксплуатации.

## About me

За последний год сфокусировалась на системном анализе и сформировала практическое портфолио вокруг одного сквозного кейса. Основной подход — доводить бизнес-сценарий до технически проверяемого решения: от требований и use cases до API-контрактов, интеграций, состояний, данных и негативных сценариев.

Ищу позицию **Junior / Junior+ System Analyst**.

## What I can do

- сбор, анализ и декомпозиция требований;
- функциональные и нефункциональные требования;
- User Stories и Use Cases;
- бизнес-правила и альтернативные сценарии;
- проектирование REST API;
- HTTP, JSON, авторизация и коды ответов;
- интеграции с внешними API и webhooks;
- асинхронные сценарии, polling и correlation ID;
- Kafka / событийное взаимодействие — в рамках проектного кейса;
- моделирование данных и SQL;
- UML, Sequence и State diagrams;
- BPMN;
- валидация данных и ФЛК;
- обработка ошибок;
- API testing / Postman;
- техническая документация.

## Featured project — U-Verse

**U-Verse** — модель облачной образовательной платформы для обучения взрослых.

В портфолио проработаны три функциональных контекста:

| Контекст | Что демонстрируется |
|---|---|
| [Система лояльности](loyalty/README.md) | баллы, промокоды, ограничения, история операций |
| [Оплата курсов](payments/README.md) | заказ, платёж, webhook, статусная модель, внешняя платёжная форма, асинхронная обработка |
| [Найм преподавателей](teacher-recruitment/README.md) | заявки, статусы, фильтрация, массовые операции, валидация и документы |

### Сквозной подход

```text
Business problem
      ↓
Requirements / User Stories
      ↓
Use Cases + Business Rules
      ↓
Data Model
      ↓
API Contract
      ↓
Integration
      ↓
States + Errors + Edge Cases
      ↓
Technical Documentation
```

## Integrations

В проектных материалах проработаны интеграционные сценарии:

- **RaifPay** — внешняя платёжная форма и webhook-сценарий;
- **T-Bank** — создание/подписание платёжного реестра и последующий polling;
- **Pruffme** — создание и редактирование вебинаров через внешнее API;
- **Kafka** — асинхронное взаимодействие в платёжном/loyalty-контуре;
- **Unisender** — отправка email-уведомлений в отдельных сценариях.

Подробнее: [Интеграции](docs/integrations.md).

## System analysis artifacts

- [Requirements](docs/requirements.md)
- [Business Rules](docs/business-rules.md)
- [Use Cases](docs/use-cases.md)
- [REST API](docs/api.md)
- [Integrations](docs/integrations.md)
- [Data Model](docs/data-model.md)
- [Diagrams](docs/diagrams.md)
- [Testing & Error Handling](docs/testing-and-errors.md)
- [Traceability matrix](docs/traceability.md)
- [Architecture & decisions](docs/architecture-decisions.md)

## Project structure

```text
.
├── README.md
├── docs/
│   ├── architecture-decisions.md
│   ├── api.md
│   ├── business-rules.md
│   ├── data-model.md
│   ├── diagrams.md
│   ├── integrations.md
│   ├── requirements.md
│   ├── testing-and-errors.md
│   ├── traceability.md
│   └── use-cases.md
├── loyalty/
│   └── README.md
├── payments/
│   └── README.md
└── teacher-recruitment/
    └── README.md
```

## Tools

**Documentation & modeling:** Markdown, PlantUML, BPMN, UML, Figma  
**API:** REST, JSON, HTTP, Swagger/OpenAPI, Postman  
**Data:** SQL, ER/data modeling  
**Project work:** Jira, Confluence  
**Integration concepts:** webhooks, Kafka, polling, external REST APIs

## AI-assisted workflow

AI использовался как инструмент ускорения подготовки и структурирования документации. Архитектурные решения, требования, бизнес-правила и итоговые артефакты проверялись и редактировались человеком.

## Contact

- LinkedIn — добавить при необходимости
- Email — добавить при необходимости
- Telegram — добавить при необходимости
- Резюме — добавить при необходимости

---

### Навигация

**[Requirements](docs/requirements.md)** · **[API](docs/api.md)** · **[Integrations](docs/integrations.md)** · **[Data Model](docs/data-model.md)** · **[Testing](docs/testing-and-errors.md)**

**[Loyalty](loyalty/README.md)** · **[Payments](payments/README.md)** · **[Teacher Recruitment](teacher-recruitment/README.md)**
