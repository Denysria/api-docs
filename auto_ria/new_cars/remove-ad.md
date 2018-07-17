## Удаление объявления

Для удаления объявления, Вам необходимо отправить **DELETE** запрос такого вида:

`curl -X DELETE "https://developers.ria.com/auto/new/autos?user_id=id&auto_id=id&api_key=YOUR_API_KEY"`
` -H "accept: application/json"`

, где *auto_id* - ваш ID в системе RIA.com, *auto_id* - id нужного Вам объявления, *api_key* - ваш ключ.

**Пример запроса**

`curl -X DELETE "https://developers.ria.com/auto/new/autos?user_id=4784009&auto_id=1696388&`
`api_key=YOUR_API_KEY" -H "accept: application/json"`

**Пример успешного ответа:**

```javascript
{"num_rows":1,
"last_insert_id":0}
```
