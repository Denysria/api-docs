### Добавление нового фильтра на обмен

 Для добавления нового фильтра на обмен в объявление, Вам необходимо выполнить POST запрос такого вида:
 
`curl -X POST "https://developers.ria.com/auto/used/autos/advertisementId/exchangeFilter?user_id=Ваш ID&api_key=YOUR_API_KEY" -H "accept: application/json" -H "content-type: application/json" -d "{\ \}"`

, где *user_id* - Ваш ID в системе RIA.com, *advertisementId* - ID нужного Вам объявления, *`-d "{ \  \  }`* - здесь Вы указываете массив параметров на обмен которые хотите добавить,  *api_key* - Ваш ключ.

**Пример запроса**

`curl -X POST "https://developers.ria.com/auto/used/autos/20438832/exchangeFilter?user_id=7069830&api_key=YOUR_API_KEY" -H "accept: application/json" -H "content-type: application/json" -d "{ \"brand\": { \"id\": 5 }, \"model\": { \"id\": 32 }, \"category\": { \"id\": 1 }, \"body\": { \"id\": 3 }, \"year\": { \"gte\": 2008, \"lte\": 2012 }}"`


**Пример успешного ответа:**

````json
{"message":"Ok","errors":[],"success":true}
````

Полное описание сервиса "Добавление нового фильтра на обмен" описаный с помощью стандарта **DeFacto swagger 2.0** [здесь](http://swagger.ria.com/ui/?api=auto/advertisements#/)
