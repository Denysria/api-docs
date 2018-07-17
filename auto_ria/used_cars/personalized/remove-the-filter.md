### Удаление существующего фильтра на обмен

Для удаления существующего фильтра на обмен, Вам необходимо выполнить DELETE запрос такого вида:

`curl -X DELETE "https://developers.ria.com/auto/used/autos/advertisementId/exchangeFilter/filterId?user_id=Ваш ID&api_key=c" -H "accept: application/json"`

, где *user_id* - Ваш ID в системе RIA.com, *advertisementId* - ID нужного Вам объявления, *filterId* - ID выбраного Вами фильтра, *api_key* - Ваш ключ.

**Пример запроса**
````javascript
curl -X DELETE "https://developers.ria.com/auto/used/autos/20438832/exchangeFilter/2930510?user_id=7069830&api_key=YOUR_API_KEY" -H "accept: application/json"`
`````
 Полное описание сервиса "Удаление существующего фильтра на обмен" описаный с помощью стандарта **DeFacto swagger 2.0** [здесь](http://swagger.ria.com/ui/?api=auto/advertisements#/)
