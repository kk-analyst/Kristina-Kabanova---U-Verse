# Kristina Kabanova

## System Analyst · Junior / Junior+

Портфолио системного аналитика на проекте **U-Verse** — облачной образовательной платформе для обучения взрослых.

Я прорабатываю требования и системные решения на стыке бизнес-логики и технической реализации: декомпозиция требований, API, интеграции, модели данных, UML/BPMN, валидация, ошибки и техническая документация.

> **Project status:** проектный кейс. Описанные решения — результаты проектирования и документирования.

## Обо мне

За последний год сфокусировалась на системном анализе и сформировала практическое портфолио вокруг одного сквозного кейса. Основной подход — доводить бизнес-сценарий до технически проверяемого решения: от требований и use cases до API-контрактов, интеграций, структуры данных и альтернативных сценариев сценариев.

Ищу позицию **Junior / Junior+ System Analyst**.

## Навыки

- сбор, анализ и декомпозиция требований;
- функциональные и нефункциональные требования;
- User Stories и Use Case;
- бизнес-правила и альтернативные сценарии;
- проектирование REST API;
- HTTP, JSON, авторизация и коды ответов;
- интеграции с внешними API и webhooks;
- асинхронные сценарии взаимодействия, polling;
- Kafka / событийное взаимодействие — в рамках проектного кейса;
- моделирование данных и SQL;
- UML, Sequence и State diagrams;
- BPMN;
- валидация данных и ФЛК;
- обработка ошибок;
- API testing / Postman;
- техническая документация.

## Проект — U-Verse

**U-Verse** — модель облачной образовательной платформы для обучения взрослых.

В портфолио проработаны три функциональных контекста:

| Контекст | Что проработано |
|---|---|
| [Система лояльности](loyalty/README.md) | баллы, промокоды, ограничения, история операций |
| [Оплата курсов](payments/README.md) | заказ, платёж, webhook, статусная модель, внешняя платёжная форма, асинхронная обработка |
| [Найм преподавателей](teacher-recruitment/README.md) | заявки, статусы, фильтрация, массовые операции, валидация и документы |

### Сквозной подход

```text
Запрос бизнес-заказчика
      ↓
Требования / User Stories
      ↓
Use Case + Бизнес-правила
      ↓
Модель данных
      ↓
API Contract
      ↓
Интеграция
      ↓
Ошибки 
      ↓
Техническая документация
```

## Интеграции

В проектных материалах проработаны интеграционные сценарии:

- **RaifPay** — внешняя платёжная форма и webhook-сценарий;
- **T-Bank** — создание/подписание платёжного реестра и последующий polling;
- **Pruffme** — создание и редактирование вебинаров через внешнее API;
- **Kafka** — асинхронное взаимодействие в платёжном контуре;
- **Unisender** — отправка email-уведомлений в отдельных сценариях.

Подробнее: [Интеграции](docs/integrations.md).

## System analysis artifacts

- [Требования](docs/requirements.md)
- [Бизнес-правила](docs/business-rules.md)
- [Use Case](docs/use-cases.md)
- [REST API](docs/api.md)
- [Интеграции](docs/integrations.md)
- [Модель данных](docs/data-model.md)
- [Диаграммы](docs/diagrams.md)
- [Тестирование & Обработка ошибок](docs/testing-and-errors.md)
- [Traceability matrix](docs/traceability.md)
- [Architecture & decisions](docs/architecture-decisions.md)

## Структура портфолио

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

**Documentation & modeling:** Markdown, PlantUML, BPMN, UML, Figma, Draw.io 
**API:** REST, JSON, HTTP, Swagger/OpenAPI, Postman  
**Data:** SQL, ER/data modeling, DBeaver, dbdiagram.io  
**Project work:** Jira, Confluence  
**Интеграция concepts:** webhooks, Kafka, polling, external REST APIs

## AI-assisted workflow

AI использовался как инструмент структурирования документации. Архитектурные решения, требования, бизнес-правила и итоговые артефакты мной проверялись и редактировались.

## Contact

- Email — laguna131kabanova@yandex.ru

---

### Навигация

**[Требования](docs/requirements.md)** · **[API](docs/api.md)** · **[Интеграции](docs/integrations.md)** · **[Модель данных](docs/data-model.md)** · **[Тестирование](docs/testing-and-errors.md)**

**[Система лояльности](loyalty/README.md)** · **[Оплата курсов](payments/README.md)** · **[Найм преподавателя](teacher-recruitment/README.md)**
