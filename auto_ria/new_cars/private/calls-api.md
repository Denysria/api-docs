## Получение данных о звонке

### GET API для получения данных о звонке

Чтобы получить данные об звонках, Вам необходимо выполнить GET запрос такого вида:

https://developers.ria.com/auto/new/calls_stat?user_id=Ваш_ID&from=ДАТА_НАЧАЛА_ВЫБОРКИ&to=ДАТА_КОНЦА_ВЫБОРКИ&api_key=YOUR_API_KEY

или 
````javascript
curl -X GET "https://developers.ria.com/auto/new/calls_stat?user_id=Ваш_ID&from=ДАТА_НАЧАЛА_ВЫБОРКИ&to=ДАТА_КОНЦА_ВЫБОРКИ&api_key=YOUR_API_KEY" -H "accept: application/json"
````
, где *user_id* - Ваш ID в системе RIA.com, *from*, *to* - фильтр по диапазону дат (год - месяц - день), *api_key* - Ваш ключ.

**Пример запроса**
````javascript
curl -X GET "https://developers.ria.com/auto/new/calls_stat?from=2021-06-01&to=2021-07-31&user_id=1505029&api_key=YOUR_API_KEY" -H "accept: application/json"
````
**Пример успешного ответа:**
[1]: 
```json
[
  {
    "call_id": 22346351,
    "caller_phone": "0951174074",
    "date": "2021-07-31T15:57:01",
    "destination_phone": "0731375686",
    "duration": 0,
    "link": "",
    "marka": "Acura",
    "marka_id": 98,
    "model": "MDX",
    "model_id": 955,
    "phone": "0730946407",
    "price": 0,
    "status": "CANCEL",
    "waighting": 11
  },
  {
    "call_id": 22345654,
    "caller_phone": "0968404829",
    "date": "2021-07-31T14:42:24",
    "destination_phone": "0731375686",
    "duration": 0,
    "link": "",
    "marka": null,
    "marka_id": 0,
    "model": null,
    "model_id": 0,
    "phone": "0504103684",
    "price": 0,
    "status": "BUSY",
    "waighting": 48
  },
  {
    "call_id": 22326708,
    "caller_phone": "0674294559",
    "date": "2021-07-30T17:00:12",
    "destination_phone": "0731375686",
    "duration": 57,
    "link": "https://track.ria.com/call_link/56w456gw45v5765ee5ser_w45/2021/07/30/380731375686=380674294559=17-00-12.wav",
    "marka": "Acura",
    "marka_id": 98,
    "model": "MDX",
    "model_id": 955,
    "phone": "0935063003",
    "price": 0,
    "status": "ANSWER",
    "waighting": 22
  },
  {
    "call_id": 22325473,
    "caller_phone": "0931426064",
    "date": "2021-07-30T15:30:21",
    "destination_phone": "0731375686",
    "duration": 0,
    "link": "",
    "marka": "Acura",
    "marka_id": 98,
    "model": "MDX",
    "model_id": 955,
    "phone": "0936073263",
    "price": 0,
    "status": "CANCEL",
    "waighting": 44
  }
]   
````
Расшифровка параметров:

- *call_id* - унильний ID звонка
- *caller_phone* - номер телефона, с которого был звонок
- *date* - Дата и время звонка
- *destination_phone* - Реальный номер на который переадресовувався звонок
- *duration* - Длительность звонка в секундах
- *link* - Ссылка на запись разговора
- *marka* - Марка, которой интересовались при разговоре
- *marka_id* - ID марки
- *model* - Модель, которой интересовались при разговоре
- *model_id* - ID модели
- *phone* - Подменный номер телефона, на который звонили
- *status* - Статус звонка (ANSWER, NOANSWER, CANCEL, BYSY, FAILED, CONGESTION)
- *waighting* - Время в секундах, прежде чем произошло соединение

______

### POST API для получения данных о звонке

Второй способ передачи данных о звонке:

1. У вас есть back-end с веб-сервером.
2. Вы передаете свой url API. (например: https://your_site.com/api/call/call_from_auto_ria).
3. Как только клиент ставит трубку, на этот адрес ми отправляем все данные. (список параметров в [п.1][1]).
4. Вы обрабатываете полученные данные на своей стороне.

