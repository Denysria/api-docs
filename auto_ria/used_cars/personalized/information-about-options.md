### Получение информации об опциях объявления

Чтобы получить информации об опциях обьявления, Вам необходимо выполнить GET запрос такого вида:

https://developers.ria.com/auto/used/autos/advertisementId/options?user_id=Ваш ID&api_key=YOUR_API_KEY

или `curl -X GET "https://developers.ria.com/auto/used/autos/advertisementId/options?user_id=Ваш ID&api_key=YOUR_API_KEY" -H "accept: application/json"`

, где *user_id* - Ваш ID в системе RIA.com, *advertisementId* - ID нужного Вам объявления, *api_key* - Ваш ключ.

**Пример запроса**
````javascript
curl -X GET "https://developers.ria.com/auto/used/autos/20438832/options?user_id=7069830&api_key=YOUR_API_KEY" -H "accept: application/json"
````
**Пример успешного ответа:**
```json
[
  {
    "id": 125
  },
  {
    "id": 137
  },
  {
    "id": 188
  },
  {
    "id": 189
  },
  {
    "id": 190
  },
  {
    "id": 191
  },
  {
    "id": 211
  },
  {
    "id": 217
  },
  {
    "id": 225
  },
  {
    "id": 303
  },
  {
    "id": 354
  },
  {
    "id": 355
  },
  {
    "id": 437
  },
  {
    "id": 463
  },
  {
    "id": 481
  },
  {
    "id": 525
  }
]
```

Для расшифровки полученых параметров можно использовать сервис [Опции](https://github.com/ria-com/auto-ria-rest-api/blob/master/AUTO_RIA_API/README.md#user-content-%D0%9E%D0%BF%D1%86%D0%B8%D0%B8)

 Полное описание сервиса "Получение информации об опциях объявления" описаный с помощью стандарта **DeFacto swagger 2.0** [здесь](http://swagger.ria.com/ui/?api=auto/advertisements#/)
