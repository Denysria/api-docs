## Поколение модели нового авто
  
Поколение зависит от модели нового авто. Следовательно список поколений можно получить  отправив GET запрос на адрес `https://developers.ria.com/auto/new/generation?model_id=id&api_key=YOUR_API_KEY`, где  *model_id* - модель выбранного авто, *api_key*- Ваш ключ.

Например, для модели BMW X6 ([https://developers.ria.com/auto/new/generation?model_id=2153&api_key=YOUR_API_KEY](https://developers.ria.com/auto/new/generation?model_id=2153&api_key=YOUR_API_KEY)), список поколений будет следующим:

```javascript
[
  {
    "year_to": 2014,
    "year_from": 2012,
    "name": "E71 (рестайлінг)",
    "model_id": 2153,
    "marka_id": 9,
    "generation_id": 432,
    "eng": "e71-restajling"
  },
  {
    "year_to": 0,
    "year_from": 2014,
    "name": "F16",
    "model_id": 2153,
    "marka_id": 9,
    "generation_id": 433,
    "eng": "f16"
  },
  {
    "year_to": 2010,
    "year_from": 2008,
    "name": "E71",
    "model_id": 2153,
    "marka_id": 9,
    "generation_id": 3275,
    "eng": "e71"
  }
]
````
