## Поиск объявлений

Чтобы обратиться к  DOM.RIA API search, Вам необходимо выполнить GET запрос такого вида:

https://developers.ria.com/dom/search?api_key=YOUR_API_KEY&PARAMETERS

или `curl -X GET "https://developers.ria.com/dom/search?api_key=YOUR_API_KEY&PARAMETERS"`
`  -H "accept: application/json"`

Он состоит из:

 * **SEARCH** — название метода API, к которому Вы хотите обратиться.

 * **API_KEY** — ключ доступа. Для получения ключа доступа нужно зарегестрироватся на портале developers.ria.com 

 * **PARAMETERS** — входные параметры, последовательность пар name=value, разделенных амперсандом. Список параметров указан выше.

В ответ на такой запрос Вы получите ответ в формате JSON:

```json
{
  "items": [                //id объявлений
    
  ],
  "count":                // количество
}
```

Полное описание сервиса "Поиск объявлений" описанный с помощью стандарта DeFacto swagger 2.0
* [Квартир](http://swagger.ria.com/ui/?api=dom/apartments)
* [Домов](http://swagger.ria.com/ui/?api=dom/house#/)
* [Коммерческой недвижимости](http://swagger.ria.com/ui/?api=dom/commercial)
* [Офисов](http://swagger.ria.com/ui/?api=dom/offices)
* [Земельных участков](http://swagger.ria.com/ui/?api=dom/land)
* [Гаражей](http://swagger.ria.com/ui/?api=dom/garages)


**Пример**

Допустим Вы ищете:
* Объект - Квартиры
* Тип недвижимости - квартира
* Операция - продажа
* Область - Киевская
* Город - Киев
* Район
   * Оболонский
   * Печерский
   * Подольский
* Количество комнат от 1 до 3
* Общая площадь от 60 до 90
* Жилая площадь от 30 до 50
* Кухня от 4 до 9
* Кухня от 3 до 7
* Год постройки - не указан
* Цена от 20000 до 90000
* Цена за объект
* Тип валюты долары США
* Возможен торг
* Тип предложения - от посредника


В итоге мы получаем запрос такого [вида]:

[https://developers.ria.com/auto/search?api_key=YOUR_API_KEY&category=1&realty_type=2&operation_type=1....](https://developers.ria.com/dom/search?category=1&realty_type=2&operation_type=1&state_id=10&city_id=10&district_id=15187&district_id=15189&district_id=15188&characteristic[209][from]=1&characteristic[209][to]=3&characteristic[214][from]=60&characteristic[214][to]=90&characteristic[216][from]=30&characteristic[216][to]=50&characteristic[218][from]=4&characteristic[218][to]=9&characteristic[227][from]=3&characteristic[227][to]=7&characteristic[443]=442&characteristic[234][from]=20000&characteristic[234][to]=90000&characteristic[242]=239&characteristic[273]=273&characteristic[1437]=1434&api_key=YOUR_API_KEY)

или `curl -X GET "https://developers.ria.com/dom/search?category=1&realty_type=2&operation_type=1&`
`state_id=10&``city_id=10&district_id=15187&district_id=15189&district_id=15188&characteristic[209][from]=1&characteristic[209][to]=3&`
`characteristic[214][from]=60&characteristic[214][to]=90&characteristic[216][from]=30&characteristic[216][to]=50&`
`characteristic[218][from]=4&characteristic[218][to]=9&characteristic[227][from]=3&characteristic[227][to]=7&`
`characteristic[443]=442&characteristic[234][from]=20000&characteristic[234][to]=90000&`
`characteristic[242]=239&characteristic[273]=273&characteristic[1437]=1434&`
`api_key=YOUR_API_KEY" -H "accept: application/json"`

В случае успешного выполнения запроса по указанным параметрам результат будет со статусом **200 OK**.

Пример успешного ответа:

```json
{
  "items": [
    13336044,
    14076392,
    13814523,
    14064249,
    13078930,
    13927706,
    13962022
  ],
  "count": 7
}
```
