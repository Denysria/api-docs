## Создание нового объявления 

 Для создания нового объявления, вам необходимо выполнить **POST** запрос такого вида:
 
`curl -X POST "https://developers.ria.com/auto/new/autos?user_id=4784009&marka_id=id&model_id=id&`
`base_id=id&equip_id=id&currency_id=id&price=цена&in_stock=id&test_drive=id&api_key=YOUR_API_KEY"`
` -H "accept: application/json"`


Обязательными параметрами являются:
- *user_id* - Ваш ID в системе RIA.com
- *marka_id* - Марка автомобиля
- *model_id* - Модель автомобиля
- *base_id* - Модификация ( базы ) по типу кузова
- *equip_id* - Комплектация автомобиля
- *currency_id* - Валюта в которой продаете автомобиль (1 - доллары США, 2 - евро, 3 - гривна)

Дополнительные параметры:
- *price* - Цена
- *auto_note* - Описание
- *version* - Версия (пример 2.0 TDI)
- *in_stock* - В наличии  (1 - в наличии, 0 - нет в наличии)
- *test_drive* - Возможность пройти тест драйв (1 - есть возможность, 0 - нету возможности)

**Пример запроса**

`curl -X POST "https://developers.ria.com/auto/new/autos?user_id=4784009&marka_id=9&model_id=2153&`
`base_id=9036&equip_id=79274&currency_id=1&price=50000&in_stock=1&test_drive=1&api_key=YOUR_API_KEY"`
` -H "accept: application/json"`

**Пример успешного ответа:**

```javascript
{
  "num_rows": 1,
  "last_insert_id": 1696388
}
```
