## Комплектации авто по модификации
    
Комплектации авто зависит от модификации (базы). Получить их список можно отправив GET запрос по адресу `https://developers.ria.com/auto/new/equip_base?base_id=id&api_key=YOUR_API_KEY`, где *base_id* - id модификации (базы), *api_key*- Ваш ключ.

Например, для модели BMW X6 E71 50i AT (407 л.с.) xDrive  ([https://developers.ria.com/auto/new/equip_base?base_id=9036&api_key=YOUR_API_KEY](https://developers.ria.com/auto/new/equip_base?base_id=9036&api_key=YOUR_API_KEY))  список комплектации будет следующим:

```javascript
[
  {
    "year": "2011",
    "name": "base",
    "equip_id": 9933,
    "base_id": 9036
  },
  {
    "year": "2012",
    "name": "base",
    "equip_id": 18668,
    "base_id": 9036
  },
  {
    "year": "2013",
    "name": "base",
    "equip_id": 26251,
    "base_id": 9036
  },
  {
    "year": "2014",
    "name": "base",
    "equip_id": 36709,
    "base_id": 9036
  },
  {
    "year": "2015",
    "name": "base",
    "equip_id": 58678,
    "base_id": 9036
  },
  {
    "year": "2016",
    "name": "base",
    "equip_id": 59806,
    "base_id": 9036
  },
  {
    "year": "2017",
    "name": "base",
    "equip_id": 79274,
    "base_id": 9036
  }
]

```
