### Изменение основной информации объявлений

Для изменения основной информации объявления, Вам необходимо отправить **PUT** запрос такого вида:

`curl -X PUT "https://developers.ria.com/auto/used/autos/advertisementId?user_id=Ваш ID&api_key=YOUR_API_KEY" -H "accept: application/json" -H "content-type: application/json"  -d "{ \  \  }`

, где *user_id* - Ваш ID в системе RIA.com, *advertisementId* - ID нужного Вам объявления, *`-d "{ \  \  }`* - здесь Вы указываете массив параметров которые хотите поменять,  *api_key* - Ваш ключ.

 Детально с параметрами и структурой можно ознакомиться [здесь](#user-content-Структура-параметров)

**Пример запроса**

Допустим Вам нужно изменить цену и валюту в которой вы продаете ваш автомобиль. Данный запрос будет иметь следующий вид:

`curl -X PUT "https://developers.ria.com/auto/used/autos/20438832?user_id=7069830&api_key=YOUR_API_KEY" -H "accept: application/json" -H "content-type: application/json" -d "{ \"price\": { \"value\":10000, \"currency\": { \"id\":1 } }}"`

или изменить главное фото объявления, данный запрос будет иметь следующий вид:

`curl -X PUT "https://developers.ria.com/auto/used/autos/20438832?user_id=7069830&api_key=YOUR_API_KEY" -H "accept: application/json" -H "content-type: application/json" -d "{  \"photos\": { \"main\": { \"id\": 16652206 } }}"`

Объект *price* включает в себя параметры *value* - значение, *currency* - ID валюты в которой вы продаете ваш автомобиль, в нашем случаи это доллар.

**Пример успешного ответа:**
```json
{"message":"Ok",

"errors":[],

"success":true}
```

 Полное описание сервиса "Изменение основной информации объявлений" описаний с помощью стандарта **DeFacto swagger 2.0** [здесь](http://swagger.ria.com/ui/?api=auto/advertisements#/)


**Важно**

Основные параметры транспортного средства доступны к редактированию на протяжении часа, после добавления на сайт:

 - “Регион”

 - “Тип транспорта”, “Марка”, “Модель”, “Версия”, “Год выпуска”

 - “VIN-номер”, “Коробка передач”, “Привод”, “Количество дверей”, “Цвет”, “Топливо”

Остальные параметры - “Цена”, “Пробег”, “Фото” автомобиля, подробное описание — можете изменять и корректировать в любое время.

Если же по истечении 60 мин.  отправить запрос на изменение одного из выше перечисленых параметров, Вы получите ошибку.

**Пример ошибки**

```json
{
   "message":"StatusCodeError: 400 - {\"message\":\"Validation failed\",\"errors\":[{\"message\":\"You can edit categories.main.id for 60 minutes\",\"code\":7},{\"message\":\"You can edit brand.id for 60 minutes\",\"code\":7},{\"message\":\"You can edit model.id for 60 minutes\",\"code\":7}]}"
}
```