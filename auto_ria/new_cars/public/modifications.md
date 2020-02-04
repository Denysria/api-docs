## Модификации (базы) по типу кузова в поколении
    
Модификация (базы) зависит от типа кузова в поколении. Получить их список можно отправив GET запрос по адресу `https://developers.ria.com/auto/new/generation_bodystyles_bases?generation_bodystyle_id=id&api_key=YOUR_API_KEY` , где *generation_bodystyle_id* - типов кузова, *api_key*- Ваш ключ.

Например, для модели BMW X6 в поколении E71 (рестайлінг) ([https://developers.ria.com/auto/new/generation_bodystyles_bases?generation_bodystyle_id=538&api_key=YOUR_API_KEY](https://developers.ria.com/auto/new/generation_bodystyles_bases?generation_bodystyle_id=538&api_key=YOUR_API_KEY)), список модификаций будет следующим:

```javascript
[
  {
    "name": "50i AT (407 л.с.) xDrive",
    "model_id": 2153,
    "marka_id": 9,
    "generation_bodystyle_id": 538,
    "base_id": 9036
  },
  {
    "name": "40d AT (306 л.с.) xDrive",
    "model_id": 2153,
    "marka_id": 9,
    "generation_bodystyle_id": 538,
    "base_id": 15821
  }
]
```
