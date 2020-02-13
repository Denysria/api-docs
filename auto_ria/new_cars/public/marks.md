## Марки

Марки зависят от типов транспорта. Поэтому для того, чтобы получить список марок необходимо отправить GET запрос по адресу `https://developers.ria.com/auto/new/marks?category_id=id&api_key=YOUR_API_KEY`, где *category_id* - идентификатор типа транспорта, *api_key*- Ваш ключ.

Например, для легковых автомобилей ([https://developers.ria.com/auto/new/marks?category_id=1&api_key=YOUR_API_KEY](https://developers.ria.com/auto/new/marks?category_id=1&api_key=YOUR_API_KEY)), результат будет следующим:
```javascript
[
  {
    "name": "Acura",
    "marka_id": 98,
    "eng": "acura",
    "country_id": 392,
    "category_id": 1
  },
  {
    "name": "Alfa Romeo",
    "marka_id": 3,
    "eng": "alfa-romeo",
    "country_id": 380,
    "category_id": 1
  },
  {
    "name": "Aston Martin",
    "marka_id": 5,
    "eng": "aston-martin",
    "country_id": 826,
    "category_id": 1
  },
  {
    "name": "Audi",
    "marka_id": 6,
    "eng": "audi",
    "country_id": 276,
    "category_id": 1
  },
  {
    "name": "Bentley",
    "marka_id": 8,
    "eng": "bentley",
    "country_id": 826,
    "category_id": 1
  },
]  
.......
```
