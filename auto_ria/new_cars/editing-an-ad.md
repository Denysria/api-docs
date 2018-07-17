## Редактирование объявления

Для редактирования основной информации объявления, вам необходимо отправить **PUT** запрос такого вида:

`curl -X PUT "https://developers.ria.com/auto/new/autos?user_id=Ваш id&auto_id=id&`
`currency_id=id&price=Цена&auto_note=Test&in_stock=id&test_drive=id&api_key=YOUR_API_KEY"`
` -H "accept: application/json" -H "Content-Length: 0"`

Обязательными параметрами являются:
- *user_id* - Ваш ID в системе RIA.com
- *auto_id* - ID нужного Вам объявления
- *currency_id* - Валюта в которой продаете автомобиль (1 - доллары США, 2 - евро, 3 - гривна)
- *Content-Length* - размер возвращаемого документа (Content-Length: 0)

Дополнительные параметры:
- *price* - Цена
- *auto_note* - Описание
- *version* - Версия (пример 2.0 TDI)
- *in_stock* - В наличии   (1 - в наличии, 0 - нет в наличии)
- *test_drive* - Возможность пройти тест драйв (1 - есть возможность, 0 - нету возможности)

**Пример запроса**

`curl -X PUT "https://developers.ria.com/auto/new/autos?user_id=4784009&auto_id=1696388&currency_id=2&`
`price=55000&auto_note=Test&in_stock=0&test_drive=0&api_key=YOUR_API_KEY"`
` -H "accept: application/json" -H "Content-Length: 0"`

**Пример успешного ответа:**

```javascript
{"num_rows":1,
"last_insert_id":0}
```
