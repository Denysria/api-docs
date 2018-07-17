### Удаление опций

Для удаления опций объявления, Вам необходимо отправить **DELETE** запрос такого вида:

`curl -X DELETE "https://developers.ria.com/auto/used/autos/advertisementId/options/ids?user_id=Ваш ID&api_key=YOUR_API_KEY" -H "accept: application/json"`

, где *user_id* - Ваш ID в системе RIA.com, *advertisementId* - ID нужного Вам объявления, "id": - ID нужной Вам опции, *api_key* - Ваш ключ.

**Пример запроса**
````javascript
curl -X DELETE "https://developers.ria.com/auto/used/autos/20438832/options/125,525,481?user_id=7069830&api_key=YOUR_API_KEY" -H "accept: application/json"`
````