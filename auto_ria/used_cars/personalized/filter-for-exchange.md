### Получение фильтров на обмен по вашему обьявлению

Для получения опций в объявление, Вам необходимо выполнить GET запрос такого вида:

https://developers.ria.com/auto/used/autos/advertisementId/exchangeFilters?user_id=Ваш ID&api_key=YOUR_API_KEY

или 
````javascript
curl -X GET "https://developers.ria.com/auto/used/autos/advertisementId/exchangeFilters?user_id=Ваш ID&api_key=YOUR_API_KEY" -H "accept: application/json"
`````
, где *user_id* - Ваш ID в системе RIA.com, *advertisementId* - ID нужного Вам объявления, *api_key* - Ваш ключ.

**Пример запроса**
````javascript
curl -X GET "https://developers.ria.com/auto/used/autos/20438832/exchangeFilters?user_id=7069830&api_key=YOUR_API_KEY" -H "accept: application/json"
`````
**Пример успешного ответа:**

````json

[
  {
    "id": 2930510,   // Id добавленного фильтра
    "brand": {
      "id": 6
    },
    "model": {
      "id": 3460
    },
    "year": {
      "lte": 2013,
      "gte": 2010
    },
    "category": {
      "id": 1
    },
    "body": {
      "id": 3
    }
  }
]
````
 Полное описание сервиса "Получение фильтров на обмен по вашему обьявлению" описаный с помощью стандарта **DeFacto swagger 2.0** [здесь](http://swagger.ria.com/ui/?api=auto/advertisements#/)

