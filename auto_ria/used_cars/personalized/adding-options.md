### Добавление опций

Для добавления опций в объявление, Вам необходимо выполнить PUT запрос такого вида:
````javascript
curl -X POST "https://developers.ria.com/auto/used/autos/advertisementId/options?user_id=Ваш ID&api_key=YOUR_API_KEY" -H "accept: application/json" -H "content-type: application/json" -d "[ { \"id\": ID опции }]"
````
, где *user_id* - Ваш ID в системе RIA.com, *advertisementId* - ID нужного Вам объявления, "id": - ID нужной Вам опции, *api_key* - Ваш ключ.

**Пример запроса**
````javascript
curl -X POST "https://developers.ria.com/auto/used/autos/20438832/options?user_id=7069830&api_key=YOUR_API_KEY" -H "accept: application/json" -H "content-type: application/json" -d "[ { \"id\": 525 }]"`
`````
**Пример успешного ответа:**
````json
{"message":"Ok",

"errors":[],

"success":true}
````
 Полное описание сервиса "Добавление опций" описаный с помощью стандарта **DeFacto swagger 2.0** [здесь](http://swagger.ria.com/ui/?api=auto/advertisements#/)
