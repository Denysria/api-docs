#### Перечень статусов заказов

Что бы получить список типов статусов нужно отправив GET запрос на адрес [https://developers.ria.com/ria/basket/status?api_key=YOUR_API_KEY](https://developers.ria.com/ria/basket/status?api_key=YOUR_API_KEY). Результат будет примерно следующим:
````javascript
 curl -X GET https://developers.ria.com/ria/basket/status?api_key=YOUR_API_KEY
````
```javascript
{
  "status": true,
  "data": [
    {
      "id": 0,
      "name": "Новые и Невыполненные"
    },
    {
      "id": 1,
      "name": "Выполненные"
    },
    {
      "id": 2,
      "name": "Невыполненные"
    },
    {
      "id": 6,
      "name": "Удаленные"
    },
    {
      "id": 4,
      "name": "Все"
    },
    {
       "id": 7,
       "name": "Обратный звонок"
     }
  ]
}
```
