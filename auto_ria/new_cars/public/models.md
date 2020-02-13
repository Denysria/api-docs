## Модели

Модели зависят от типов транспорта и марок. Следовательно список марок можно получить по адресу `https://developers.ria.com/auto/new/models?marka_id=id&category_id=id&api_key=YOUR_API_KEY`, где *category_id* - идентификатор типа транспорта а *marka_id* - идентификатор марки, *api_key*- Ваш ключ.

Например, для легкового автомобиля BMW ([https://developers.ria.com/auto/new/models?marka_id=9&category_id=1&api_key=YOUR_API_KEY](https://developers.ria.com/auto/new/models?marka_id=9&category_id=1&api_key=YOUR_API_KEY)), список моделей будет следующим:
```javascript
[
  {
    "parent_id": 0,
    "name": "1 Series",
    "model_id": 2161,
    "marka_id": 9,
    "eng": "1-series",
    "category_id": "1"
  },
  {
    "parent_id": 0,
    "name": "2 Series",
    "model_id": 43023,
    "marka_id": 9,
    "eng": "2-series",
    "category_id": "1"
  },
  {
    "parent_id": 0,
    "name": "3 Series",
    "model_id": 3219,
    "marka_id": 9,
    "eng": "3-series",
    "category_id": "1"
  },
  {
    "parent_id": 3219,
    "name": "3 Series GT",
    "model_id": 43029,
    "marka_id": 9,
    "eng": "3-series-gt",
    "category_id": "1"
  },
  {
    "parent_id": 0,
    "name": "4 Series",
    "model_id": 42495,
    "marka_id": 9,
    "eng": "4-series",
    "category_id": "1"
  },
]  
.......
````
