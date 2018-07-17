### Типы привода

Типы привода также зависят от тиа транспорта, поэтому, чтобы получить их список, необходимо плсать GET запрос по адресу `https://developers.ria.com/auto/categories/:categoryId/driverTypes?api_key=YOUR_API_KEY`, где *categoryId* - идентификатор типа транспорта, *api_key*- Ваш ключ.

Например, список типов привода для мотоциклов ([https://developers.ria.com/auto/categories/2/driverTypes?api_key=YOUR_API_KEY](https://developers.ria.com/auto/categories/2/driverTypes?api_key=YOUR_API_KEY)) выглядит следующим образом:
```javascript
[
    { name: "Кардан", value: 4 },
    { name: "Ремень", value: 5 },
    { name: "Цепь", value: 6 }
]
```
