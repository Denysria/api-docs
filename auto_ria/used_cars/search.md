# API Поиска


Чтобы обратиться к  RIA API search, Вам необходимо выполнить GET запрос такого вида:

https://developers.ria.com/auto/search?api_key=YOUR_API_KEY&PARAMETERS

или `curl -i -g -X GET "https://developers.ria.com/auto/search?api_key=YOUR_API_KEY&PARAMETERS" '`

Он состоит из:

 * **SEARCH** — название метода API, к которому Вы хотите обратиться.

 * **API_KEY** — ключ доступа. Для получения ключа доступа нужно зарегестрироватся на портале dev.ria.com 

 * **PARAMETERS** — входные параметры, последовательность пар name=value, разделенных амперсандом. Список параметров указан  [здесь](#user-content-Список-параметров)
 

В ответ на такой запрос Вы получите ответ в формате JSON:

```javascript
[
 {
  "additional_params": {
    "lang_id": 2,                                             // Русский язык
    "page": 0,                                                // Порядеовый номер страницы
    "view_type_id": 0,
    "target": "search",
    "section": "auto",                                        // Поиск по авто
    "catalog_name": "",
    "elastica": true,
    "nodejs": true
  },
  "result": {                                                // Результат поиска
    "search_result": {
      "ids": [                                               // id объявлений
        ....
        ....
        ....
        
      ],
      "count": 11,                                          // Количество id объявлений доступных по заданым параметрам
      "last_id": 0,
      "qs": {
        "fields": [
          "_id"
        ],
        "size": 50,                                         // Количество отображаемых id объявлений
        "from": 0,  
 ]
```

## Пример

Допустим Вы ищете:

* Легковые машины                                            ``(category_id=1)``
* Кузов *Седан*,*Универсал*                                 `(bodystyle[0]=3&bodystyle[4]=2)`
* Япония                                                   `(brandOrigin[0]=276)`
    * Toyota                                               ` (marka_id[0]=79)`
    * Все модели                                            `(model_id[0]=0)`
    * Год выпуска от 2010 по 2017г.                        ` (s_yers[0]=2010&po_yers[0]=2017)`
* Германия                                                  `(brandOrigin[1]=392)`
    * Volkswagen                                            `(marka_id[1]=84)`
    * Все модели                                            `(model_id[1]=0)`
    * Год выпуска от 2012 по 2016г.                        `(s_yers[1]=2012&po_yers[1]=2016)`      
* Цена от 1000 до 60000                                     `(price_ot=1000&price_do=60000)`
    * Цена указана в доларах США                           ` (currency=1)`
* Возможен торг                                             `(auctionPossible=1)`
* Возможен обмен на недвижимость                           ` (with_real_exchange=1)`
* Возможен обмен на автомобиль                             ` (with_exchange=1)`
    * Марка автомобиля любая                               ` (exchange_filter[marka_id]=0)`
    * Модель автомобиля любая                              ` (exchange_filter[model_id]=0)`
* Область
    * Винницкая - поиск по всем городам этой области       ` (state[0]=1&city[0]=0)`
    * Житомирская - поиск по всем городам этой области     ` (state[1]=2&city[1]=0)`
    * Киевская - поиск по всем городам этой области        ` (state[2]=10&city[2]=0)`
* Не отображать авто которые находяться не в Украине       ` (abroad=2)`
* Не отображать нерастаможенные авто                       ` (custom=1)`
* Гаражное хранение                                         `(auto_options[477]=477)`
* Топливо
    * Бензин                                                `(type[0]=1)`
    * Дизель                                                `(type[1]=2)`
    * Газ/бензин                                            `(type[3]=4)`
    * Электро                                               `(type[5]:6)`
* КПП
    * Ручная / Механика                                     `(gearbox[0]=1)`
    * Автомат                                               `(gearbox[1]=2)`
    * Типтроник                                             `(gearbox[2]=3)`
* Объем 1.4 - 3.2 л.                                        `(engineVolumeFrom=1.4&engineVolumeTo=3.2)`
* Мощность 90 - 250                                         `(powerFrom=90&powerTo=250)`
    * Единица измерения мощности - л.с                      `(power_name=1)`
* Только с фото                                             `(with_photo=1)`

В итоге мы получаем запрос такого [вида]:

[https://developers.ria.com/auto/search?api_key=YOUR_API_KEY&category_id=1&bodystyle[0]=3&....](https://developers.ria.com/auto/search?api_key=YOUR_API_KEY&category_id=1&bodystyle[0]=3&bodystyle[4]=2&marka_id[0]=79&model_id[0]=0&s_yers[0]=2010&po_yers[0]=2017&marka_id[1]=84&model_id[1]=0&s_yers[1]=2012&po_yers[1]=2016&brandOrigin[0]=276&brandOrigin[1]=392&price_ot=1000&price_do=60000&currency=1&auctionPossible=1&with_real_exchange=1&with_exchange=1&exchange_filter[marka_id]=0&exchange_filter[model_id]=0&state[0]=1&city[0]=0&state[1]=2&city[1]=0&state[2]=10&city[2]=0&abroad=2&custom=1&auto_options[477]=477&type[0]=1&type[1]=2&type[3]=4&type[7]=8&gearbox[0]=1&gearbox[1]=2&gearbox[2]=3&engineVolumeFrom=1.4&engineVolumeTo=3.2&powerFrom=90&powerTo=250&power_name=1&countpage=50&with_photo=1)


В случае успешного выполнения запроса по указанным параметрам результат будет со статусом **200 OK**.

Пример успешного ответа:
```javascript
[
    {
   "additional_params": {
     "lang_id": 2,                                  // Русский язык
     "page": 0,                                     // Порядеовый номер страницы
     "view_type_id": 0,
     "target": "search",
     "section": "auto",                             // Поиск по авто
     "catalog_name": "",
     "elastica": true,
     "nodejs": true
   },
   "result": {                                      // Результат поиска
     "search_result": {
       "ids": [
         "19519211",
         "19684763",
         "19493489",
         "19714833",
         "19393702",
         "19692238",                                // id объявлений
         "19574398",
         "18154136",
         "19391327",
         "18693600",
         "19431563",
         "18047892"
       ],
       "count": 1,                                 // Количество id объявлений доступных по заданым параметрам
       "last_id": 0, 
       "qs": {
         "fields": [
           "_id"
         ],
         "size": 50,                                // Количество отображаемых id объявлений
         "from": 0,
             } 
            }     
           }
   }   
 ]
```


**Важно**

Максимальное количество отображаемых id объявлений за один запрос равно 100(*countpage*).В случае если результат 
поиска превышает это значение можно добавить параметр *page* (порядковый номер страницы) c помощью которго можно 
просматреть все результаты поиска.

```
"additional_params": {
    "lang_id": 2,
    "page": "1",                           // Порядковый номер страницы     
    "view_type_id": 0,
    "target": "search",
    "section": "auto",
    "catalog_name": "",
    "elastica": true,
    "nodejs": true
  },
  "result": {
    "search_result": {
      "ids": [
        "19885907",
        "19885290",
        "19847856",
        "19876230",
        "19662019",
        "18493054",
        "19440597",
        "19865852",
        "18814906",
        "19862470",
        "19738583",
       . . . . . . .     
        "19860637",
        "19747721",
        "18050784",
        "19810589",
        "19746765",
        "18412097",
        "18545537"
      ],
      "count": 1578,                         // Количество id по результатам поиска
      "last_id": 0,
      "qs": {
        "fields": [
          "_id"
        ],
        "size": 100,
        "from": 100,
```

Параметры поиска на сайте AUTO.RIA отличаются от параметров указанных ниже. Для использования параметров поиска с сайта AUTO.RIA
нужно обратиться к сервису конфигурации новых параметров в старые.

*Пример*

Допустим Вам нужен список автомобилей по параметрам указаных ниже:

[https://auto.ria.com/search/?categories.main.id=1&brand.id[0]...](https://auto.ria.com/search/?categories.main.id=1&brand.id[0]=9&year[0].gte=2011&year[0].lte=2016&custom.not=1&fuel.id[5]=6&gearbox.id[1]=2&gearbox.id[2]=3&size=10"&countpage=100)


Используем сервис конфигурации

[https://developers.ria.com/new_to_old?api_key=YOUR_API_KEY&categories.main.id=1&brand.id...](https://developers.ria.com/new_to_old?api_key=YOUR_API_KEY&categories.main.id=1&brand.id[0]=9&year[0].gte=2011&year[0].lte=2016&custom.not=1&fuel.id[5]=6&gearbox.id[1]=2&gearbox.id[2]=3&size=10"&countpage=10)


В результате мы получим параметры которые сможем применять в API Search:
```json
{
  "unrecognized": {
    "countpage": "100"
  },
  "converted": {
    "category_id": "1",
    "marka_id[0]": "9",
    "model_id[0]": "0",
    "s_yers[0]": "2011",
    "po_yers[0]": "2016",
    "custom": "1",
    "type[5]": "6",
    "gearbox[1]": "2",
    "gearbox[2]": "3",
    "countpage": "10\""
  },
  "string": "category_id=1&marka_id%5B0%5D=9&model_id%5B0%5D=0&s_yers%5B0%5D=2011&po_yers%5B0%5D=2016&custom=1&type%5B5%5D=6&gearbox%5B1%5D=2&gearbox%5B2%5D=3&countpage=10%22"
}

```
Этот запрос можно производить и в обратном порядке:

Используем сервис конфигурации

[https://developers.ria.com/old_to_new?api_key=YOUR_API_KEY&category_id=1&marka_id[0]=9...](https://developers.ria.com/old_to_new?api_key=YOUR_API_KEY&category_id=1&marka_id[0]=9&model_id[0]=0&s_yers[0]=2011&po_yers[0]=2016&custom=1&type[5]=6&gearbox[1]=2&gearbox[2]=3&countpage=100)


В результате мы получим новые параметры которые можем использовать на сайте AUTO.RIA
```json
{
  "unrecognized": {
    
  },
  "converted": {
    "categories.main.id": "1",
    "brand.id[0]": "9",
    "year[0].gte": "2011",
    "year[0].lte": "2016",
    "custom.not": "1",
    "fuel.id[5]": "6",
    "gearbox.id[1]": "2",
    "gearbox.id[2]": "3",
    "size": "100"
  },
  "string": "categories.main.id=1&brand.id%5B0%5D=9&year%5B0%5D.gte=2011&year%5B0%5D.lte=2016&custom.not=1&fuel.id%5B5%5D=6&gearbox.id%5B1%5D=2&gearbox.id%5B2%5D=3&size=100"
}
```
