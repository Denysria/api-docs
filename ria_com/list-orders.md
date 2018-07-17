#### Перечень заказов 

Что бы получить список заказов нужно отправив GET запрос на адрес [https://developers.ria.com/ria/basket/orders/?api_key=YOUR_API_KEY](https://developers.ria.com/ria/basket/orders/?api_key=YOUR_API_KEY).
````javascript
  curl -X GET https://developers.ria.com/ria/basket/orders?api_key=YOUR_API_KEY
 ````
 Результат будет примерно следующим:

```javascript
{
   "status":true,
   "total":2,
   "orders":[
     {
       "order_id":21,                         // id заказа
       "status":6,                            // Статус "Удаленные"
       "total_order_sum":100,                 // Общая сумма заказа
       "created_at":"2017-04-06 16:35:31",    // Время создания
       "recipient":{
         "user_id":000000,                    // id пользователя
         "name":"Андрій Сергійович",
         "email":"mail@gmail.com",
         "phone":"......"                     // Телефон
       },
       "delivery":{                           // Доставка
          "state_id":1,                       // id Области
         "city_id":1,                         // id Города
         "address":"Винницкая область, Винница",
         "service":"DHL"                      // Служба доставки
         "department":"Отделение №1: ул. Интернациональная, 20а"  // Информация об отделении
       },
       "items":[
         {
           "adv_id":3612261,                  // id объявления
           "name":"Детали двигателя Головка блока Легковой Audi A3 Cabrio v2 v3",
           "price":100,                       // Цена
           "count":1,                         // Количество
           "note":""                          // Заметки
           "vendor_code": ""                  // Код поставщика
         }
       ]
     },
     ...
   ]
```
