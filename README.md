# Lab 3 — Комплексне тестування REST API із використанням Postman

## Автор

**Сахно Данило Олександрович**
Київський національний університет імені Тараса Шевченка
Факультет комп’ютерних наук та кібернетики
Спеціальність: **Інженерія програмного забезпечення**

---

## Мета роботи

Набуття практичних навичок комплексного тестування REST API, включаючи функціональне тестування, валідацію JSON Schema, сценарне тестування, негативні перевірки, параметризоване тестування та автоматизацію запуску через Newman.

---

## Використані технології

* **Postman**
* **Newman CLI**
* **JSONPlaceholder API**
* **CSV**
* **JavaScript (Postman Scripts)**
* **Node.js**
* **HTML Reporter**

---

## Тестований сервіс

```text
https://jsonplaceholder.typicode.com
```

---

## Структура колекції

```text
Lab3RestApiTesting/
├── Functional tests
│   ├── GET /posts
│   ├── GET post by id - schema validation
│   ├── POST data-driven test
│
├── Workflow
│   ├── POST create post
│   ├── GET created post
│   ├── PUT update post
│   ├── GET updated post
│   ├── DELETE post
│
├── Negative tests
│   ├── GET non-existing resource
│   ├── POST invalid data
│   ├── PUT wrong id
│   ├── DELETE non-existing resource
│
├── data.csv
├── collection.json
├── environment.json
├── newman-run-report.html
└── README.md
```

---

## Реалізовані тестові сценарії

У межах лабораторної роботи реалізовано **14 тестових сценаріїв**:

* **AT-01** — GET /posts verification
* **AT-02** — response structure validation
* **AT-03** — JSON Schema validation
* **AT-04** — data-driven POST testing
* **AT-05** — workflow POST → GET → PUT → DELETE
* **AT-06** — pre-request random data generation
* **AT-07** — GET non-existing resource
* **AT-08** — POST invalid data
* **AT-09** — PUT wrong ID
* **AT-10** — DELETE wrong ID
* **AT-11** — response time validation
* **AT-12** — logging and variable storage
* **AT-13** — stability analysis
* **AT-14** — quality metrics calculation

---

## Результати виконання тестів

| ID    | Назва тесту          | Статус |
| ----- | -------------------- | ------ |
| AT-01 | GET /posts           | Pass   |
| AT-02 | Structure Validation | Pass   |
| AT-03 | JSON Schema          | Pass   |
| AT-04 | Data-driven POST     | Pass   |
| AT-05 | Workflow             | Pass   |
| AT-06 | Pre-request Script   | Pass   |
| AT-07 | Negative GET         | Pass   |
| AT-08 | Negative POST        | Pass   |
| AT-09 | Negative PUT         | Pass   |
| AT-10 | Negative DELETE      | Pass   |
| AT-11 | Performance          | Pass   |
| AT-12 | Logging              | Pass   |
| AT-13 | Stability            | Pass   |
| AT-14 | Metrics              | Pass   |

---

## Підсумок

* **Всього тестів:** 14
* **Успішно:** 14
* **Помилок:** 0
* **Failures:** 0

---

## Метрики якості API

* **Середній response time:** 35–40 ms
* **Відсоток успішних тестів:** 100%
* **Кількість помилок:** 0

API продемонстрував стабільну роботу без критичних відхилень.

---

## Автоматизація

Колекція була успішно виконана через **Newman CLI**:

```bash
newman run "New Collection.postman_collection.json" -e "JsonPlaceholder Lab.postman_environment.json" -r cli,html
```

---

## HTML звіт

Результати автоматизованого тестування збережені у файлі:

```text
newman-run-report.html
```

---

## Висновок

У результаті виконання лабораторної роботи було реалізовано комплексне тестування REST API із використанням **Postman та Newman**.

Було створено повноцінний набір тестів для функціональної перевірки API, негативних сценаріїв, workflow тестування, schema validation, data-driven тестування та автоматизованого запуску.

Усі тестові сценарії були успішно виконані, що підтверджує коректність реалізованої логіки тестування та стабільність роботи API.
