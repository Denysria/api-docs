#### Изменение статуса заказа

Что бы изменить статус заказа нужно отправить PUT запрос на адрес
````javascript
curl -X PUT "https://developers.ria.com/ria/basket/orders?user_id=*id*&order_id=*id*&api_key=YOUR_API_KEY" -H "accept: application/json" -H "content-type: application/json"
 -d "{ \"status\": 0}"
 `````
 , где *user_id* - id пользователя, *order_id* - id заказа, *status_id* - id статуса заказа, 

 
 
 Ответ будет следующим:
```javascript
{
  "status": true
}
```
