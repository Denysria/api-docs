### Марки

Марки зависят от типов транспорта. Поэтому для того, чтобы получить список марок необходимо отправить GET запрос по адресу `https://developers.ria.com/auto/categories/:categoryId/marks?api_key=YOUR_API_KEY`, где *categoryId* - идентификатор типа транспорта, *api_key*- Ваш ключ.

Например, для легковых автомобилей ([https://developers.ria.com/auto/categories/1/marks?api_key=YOUR_API_KEY](https://developers.ria.com/auto/categories/1/marks?api_key=YOUR_API_KEY)), результат будет следующим:
```javascript
[
    { name: "Acura", value: 98 },
    { name: "Adler", value: 2396 },
    { name: "Aixam", value: 2 },
    { name: "Alfa Romeo", value: 3 },
    { name: "Alpine", value: 100 },
    { name: "Altamarea", value: 3988 },
    { name: "Aro", value: 101 },
    { name: "Artega", value: 3105 },
    { name: "Asia", value: 4 },
    { name: "Aston Martin", value: 5 },
    { name: "Audi", value: 6 },
    { name: "Austin", value: 7 },
    { name: "Autobianchi", value: 102 }
    ...
]
```
