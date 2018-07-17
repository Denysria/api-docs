### Опции

Опции зависят от типа транспорта. Получить их список можно отправив GET запрос по адресу `https://developers.ria.com/auto/categories/:categoryId/options?api_key=YOUR_API_KEY`, где *categoryId* - идентификатор типа транспорта, *api_key*- Ваш ключ.

Например, список опций для легковых автомобилей ([https://developers.ria.com/auto/categories/1/options?api_key=YOUR_API_KEY](https://developers.ria.com/auto/categories/1/options?api_key=YOUR_API_KEY)) будет выглядеть примерно так:
```javascript
[
    { name: "ABD", value: 354 },
    { name: "ABS", value: 217 },
    { name: "ESP", value: 459 },
    { name: "Галогенные фары", value: 463 },
    { name: "Замок на КПП", value: 481 },
    { name: "Иммобилайзер", value: 225 },
    { name: "Пневмоподвеска", value: 442 },
    { name: "Подушка безопасности (Airbag)", value: 211 },
    { name: "Серворуль", value: 485 },
    { name: "Сигнализация", value: 303 },
    ...
]
```
