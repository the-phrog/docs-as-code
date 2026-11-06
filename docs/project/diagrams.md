# Диаграммы

## Диаграмма последовательности

```mermaid
sequenceDiagram
    actor Client as Клиент
    participant App as Система
    participant Model as ML-модель
    Client->>App: Отправить отзыв
    App->>App: Проверить непустой текст и определить язык
    alt Английский язык подтверждён
        App->>Model: Передать англоязычный текст
        Model-->>App: Вернуть тональность
        App-->>Client: Сохранить и показать результат
    else Другой или неопределённый язык
        App-->>Client: HTTP 422 — поддерживается только английский язык
    end
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
