### Удаление объявления

Для удаления объявления, Вам необходимо отправить **DELETE** запрос такого вида:
````javascript
curl -X DELETE "https://developers.ria.com/auto/used/autos/advertisementId?user_id=Ваш ID&reason_id=id причины удаления&api_key=YOUR_API_KEY" -H "accept: application/json"
`````
, где *user_id* - Ваш ID в системе RIA.com, *advertisementId* - ID нужного Вам объявления, *reason_id* - причина удаления, *api_key* - Ваш ключ.

**reason_id** состоит из 4 категорий:
- **reason_id**=**4** - Авто продано с помощью AUTO.RIA.com
- **reason_id**=**5** - Авто продано в другом месте
- **reason_id**=**6** - Я хочу разместить объявление заново
- **reason_id**=**7** - Я передумал продавать автомобиль

**Пример запроса**
````javascript
curl -X DELETE "https://developers.ria.com/auto/used/autos/20460133?user_id=7069830&reason_id=7&api_key=YOUR_API_KEY" -H "accept: application/json"`
`````
 Полное описание сервиса "Удаление объявления" описаный с помощью стандарта **DeFacto swagger 2.0** [здесь](http://swagger.ria.com/ui/?api=auto/advertisements#/)
