# Диаграммы

## Диаграмма последовательности

```mermaid
sequenceDiagram
    actor Client as Клиент
    participant App as Система
    participant Model as ML-модель
    Client->>App: Отправить отзыв
    App->>Model: Передать текст
    Model-->>App: Вернуть тональность
    App-->>Client: Показать результат
```

## Диаграмма классов

```mermaid
classDiagram
    class User {
        +int id
    }
    class Review {
        +int id
        +string text
    }
    class Analysis {
        +int id
        +string sentiment
    }
    User "1" --> "*" Review
    Review "1" --> "1" Analysis
```
