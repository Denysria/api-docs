### Список объявлений пользователя

Чтобы получить список объявлений, Вам необходимо выполнить GET запрос такого вида:

https://developers.ria.com/auto/used/autos/ids?user_id=Ваш ID в системе RIA.com&api_key=YOUR_API_KEY

или `curl -X GET "https://developers.ria.com/auto/used/autos/ids?user_id=Ваш ID&api_key=YOUR_API_KEY" -H "accept: application/json"`

, где *user_id* - Ваш ID в системе RIA.com, *api_key* - Ваш ключ.

**Пример запроса**
````javascript
curl -X GET "https://developers.ria.com/auto/used/autos/ids?user_id=7069830&api_key=YOUR_API_KEY" -H "accept: application/json"
`````
**Пример успешного ответа:**

```json
{
  "active": {
    "moderated": [

    ],
    "notModerated": [

    ]
  },
  "draft": [

  ],
  "awaitingPayment": [

  ],
  "archive": [
    20438832,
    20445742
  ]
}
```
Расшифровка параметров:
 - *active* - Активные объявления
 - *moderated* - Объявления находятся на модерации
 - *notModerated* - Объявления не от модерировано
 - *draft* - Объявления находятся в черновиках
 - *awaitingPayment* - Объявления ожидают оплаты
 - *archive* - Объявления в архиве

Полное описание сервиса "Список объявлений пользователя" описаний с помощью стандарта **DeFacto swagger 2.0** [здесь](http://swagger.ria.com/ui/?api=auto/advertisements#/)
