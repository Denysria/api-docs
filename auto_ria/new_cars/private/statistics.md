## Статистика объявления

Чтобы получить статистику об обьявлении, Вам необходимо выполнить GET запрос такого вида:

https://developers.ria.com/auto/new/stat?user_id=Ваш ID&auto_id=ID объявления&date_from= дата с&date_to=дата по&api_key=YOUR_API_KEY

или 
````javascript
curl -X GET "https://developers.ria.com/auto/new/stat?user_id=Ваш ID&auto_id=ID объявления&date_from= фильтр по диапазону дат&date_to=фильтр по диапазону дат&api_key=YOUR_API_KEY" -H "accept: application/json"
````
, где *user_id* - Ваш ID в системе RIA.com, *auto_id* - ID нужного Вам объявления, *date_from*, *date_to* - фильтр по диапазону дат (год - месяц - день),*api_key* - Ваш ключ.

**Пример запроса**
````javascript
curl -X GET "https://developers.ria.com/auto/new/stat?user_id=4784009&auto_id=1696177&date_from=2018-03-06&date_to=2018-07-10&api_key=YOUR_API_KEY" -H "accept: application/json"
````
**Пример успешного ответа:**

```json
{
  "viewsStatistics": [
    {
      "salon_id": 2407,
      "model_id": 1038,
      "marka_id": 13,
      "date": "2018-05-15",
      "count": 1,
      "auto_id": 1696177,
      "type": "views"
    },
    {
      "salon_id": 2407,
      "model_id": 1038,
      "marka_id": 13,
      "date": "2018-05-20",
      "count": 105,
      "auto_id": 1696177,
      "type": "views"
    },
    {
      "salon_id": 2407,
      "model_id": 1038,
      "marka_id": 13,
      "date": "2018-03-09",
      "count": 23,
      "auto_id": 1696177,
      "type": "views"
    },
    {
      "salon_id": 2407,
      "model_id": 1038,
      "marka_id": 13,
      "date": "2018-04-27",
      "count": 1,
      "auto_id": 1696177,
      "type": "views"
    },
    {
      "salon_id": 2407,
      "model_id": 1038,
      "marka_id": 13,
      "date": "2018-03-08",
      "count": 30,
      "auto_id": 1696177,
      "type": "views"
    }
  ],
  "phonesStatistics": [
      {
        "salon_id": 2407,
        "model_id": 1038,
        "marka_id": 13,
        "date": "2018-04-15",
        "count": 1,
        "auto_id": 1696177,
        "type": "auto_phones_final"
      },
      {
        "salon_id": 2407,
        "model_id": 1038,
        "marka_id": 13,
        "date": "2018-04-14",
        "count": 1,
        "auto_id": 1696177,
        "type": "auto_phones_final"
      },
      {
        "salon_id": 2407,
        "model_id": 1038,
        "marka_id": 13,
        "date": "2018-06-03",
        "count": 1,
        "auto_id": 1696177,
        "type": "auto_phones_final"
      },
      {
        "salon_id": 2407,
        "model_id": 1038,
        "marka_id": 13,
        "date": "2018-05-21",
        "count": 21,
        "auto_id": 1696177,
        "type": "auto_phones_final"
      }
   ]   
````
Расшифровка параметров:

- *viewsStatistics* - Количество просмотров объявления 
- *phonesStatistics* - Количество открытий номера телефона
- *salon_id* - id салона
- *model_id* - id модели автомобиля
- *marka_id* - id марки автомобиля
- *date* - дата
- *count* -количество
- *auto_id* - id объявления
- *type* - "views" - Просмотры объявления
- *type* - "auto_phones_final" - Открытие номеров телефона


 Полное описание сервиса "Статистика объявления" описаный с помощью стандарта **DeFacto swagger 2.0** [здесь](http://swagger.ria.com/ui/?api=auto/newauto_salon_api#/)


