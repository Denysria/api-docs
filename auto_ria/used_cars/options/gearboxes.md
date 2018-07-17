### Коробки передач

Коробки передач зависят от типа транспорта, поэтому, чтобы получить их список, необходимо послать GET запрос по адресу `https://developers.ria.com/auto/categories/:categoryId/gearboxes?api_key=YOUR_API_KEY`, где *categoryId* - идентификатор типа транспорта, *api_key*- Ваш ключ .

Например, список коробок передач для мотоциклов ([https://developers.ria.com/auto/categories/2/gearboxes?api_key=YOUR_API_KEY](https://developers.ria.com/auto/categories/2/gearboxes?api_key=YOUR_API_KEY)) будет выглядеть следующим образом:
```javascript
[
    { name: "Ручная / Механика", value: 1 },
    { name: "Автомат", value: 2 },
    { name: "Типтроник", value: 3 },
    { name: "Адаптивная", value: 4 },
    { name: "Вариатор", value: 5 }
]
```
