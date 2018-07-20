## Типы кузова в поколении новых авто
    
Тип кузова зависит от поколения авто. Поэтому для того, чтобы получить список типов кузова необходимо отправить GET запрос на адрес `https://developers.ria.com/auto/new/generation_bodystyles?generation_id=id&api_key=YOUR_API_KEY` , где *generation_id* - поколение авто, *api_key*- Ваш ключ.

Например, для модели BMW X6 в поколении E71 (рестайлинг) ([https://developers.ria.com/auto/new/generation_bodystyles?generation_id=432&api_key=YOUR_API_KEY](https://developers.ria.com/auto/new/generation_bodystyles?generation_id=432&api_key=YOUR_API_KEY)), список типов кузова будет следующим:

```javascript
[
  {
    "generation_bodystyle_id": 538,
    "bodystyle_id": 324
  }
]
```
