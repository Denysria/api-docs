# AUTO info  Информация по id объявления

Чтобы обратиться к  RIA API info, Вам необходимо выполнить GET запрос такого вида:

https://developers.ria.com/auto/info?api_key=YOUR_API_KEY&auto_id=**id_объявления**

или  `curl -i -X GET "https://developers.ria.com/auto/info?api_key=YOUR_API_KEY&auto_id=id_объявления"`

Он состоит из:

 * **info** — название метода API, к которому Вы хотите обратиться.
 
 * **API_KEY** — ключ доступа. Для получения ключа доступа нужно зарегестрироватся на портале developers.ria.com 

 * **auto_id=** — номер объявления по которому нужна информация
 
## Пример

Допусти Вам нужна информация по _19050985_ id.

Данный запрос будет выглядеть так:

https://developers.ria.com/auto/info?api_key=YOUR_API_KEY&auto_id=19050985

или  `curl -i -X GET "https://developers.ria.com/auto/info?api_key=YOUR_API_KEY&auto_id=19050985"`

В случае успешного выполнения запроса  результат будет со статусом **200 OK**.

Пример успешного ответа:

```javascript
[
 {
  "userId": 489269,                                                                       // id пользователя
  "chipsCount": 0,
  "locationCityName": "Днепропетровск",                                                   // Город
  "auctionPossible": false,                                                               // Торг 
  "exchangePossible": false,                                                              // Обмен    
  "realtyExchange": false,                                                                // Обмен на надвижимость 
  "exchangeType": "Любой",                                                                // Тип обмена
  "exchangeTypeId": 0,                                                                    // Идентификатор типа обмена
  "addDate": "2017-04-24 23:02:06",                                                       // Дата и время добавления 
  "updateDate": "2017-04-24 23:02:06",                                                    // Дата и время обновления 
  "expireDate": "2017-07-24 23:02:06",                                                    // Дата и время истечения
  "userHideADSStatus": false,                                                             // Пользователь скрыл статус
  "userPhoneData": {
    "phoneId": "3336492",                                                                 // id телефона пользователя 
    "phone": "(067) 522-60-77"                                                            // Телефон пользователя
  },
  "USD": 33500,                                                                           // Стоимость в доларах США
  "UAH": 880380,                                                                          // Стоимость в гривнах
  "EUR": 30815,                                                                           // Стоимость в евро
  "isAutoAddedByPartner": false,                                                          
  "partnerId": 0, 
  "levelData": {
    "level": 10,                                                                          // Уровень топа
    "label": 3,                                                                           // Метка
    "hotType": "срочно",                                                                  // Метка "TOP" или "Срочно"
    "expireDate": "2017-05-04 23:02:07"                                                   // Дата и время истечения метки "тор" "Срочно"
  },
  "autoData": {                                                                           // Характеристики машины
    "description": "Итак. Пришло время в срочном порядке продать свой любимый автомобиль. " +
     "\r\nПокупал его в августе 2013 года. \r\nПолностью обслужен на о",                  // Описание
    
    "version": "",
    "onModeration": false,
    "year": 2013,                                                                         // Год выпуска
    "autoId": 19050985,                                                                   // id объявления
    "statusId": 0,                                                                        //  - 
    "withVideo": false,                                                                   // Наличие видео                               
    "race": "60 тыс. км",                                                                 // Пробег
    "raceInt": 60,                                                                        // - 
    "fuelName": "Дизель",                                                                 // Тип топлива
    "gearboxName": "Автомат",                                                             // Тип привода
    "isSold": false,                                                                      // Этот параметр показывает или машына продана или нет
    "mainCurrency": "USD",                                                                // Основная валюта
    "fromArchive": false,
    "categoryId": 1,                                                                      // Тип транспорта
    "custom": 0                                                                           
  },
  "markName": "Volvo",                                                                    // Марка автомобиля
  "markId": 85,                                                                           // id марки автомобиля
  "modelName": "XC90",                                                                    // Модель автомобиля
  "modelId": 824,                                                                         // id Модели автомобиля
  "photoData": {                                                                          // Фотографии
    "count": 15,                                                                          // Количество фотографий
    "seoLinkM": "https://cdn.riastatic.com/photosnew/auto/photo/volvo_xc90__181949196m.jpg",
    "seoLinkSX": "https://cdn.riastatic.com/photosnew/auto/photo/volvo_xc90__181949196sx.jpg",
    "seoLinkB": "https://cdn.riastatic.com/photosnew/auto/photo/volvo_xc90__181949196b.jpg",
    "seoLinkF": "https://cdn.riastatic.com/photosnew/auto/photo/volvo_xc90__181949196f.jpg"
  },
  "linkToView": "/auto_volvo_xc90_19050985.html",                                         // Линк на объявление
  "title": "Volvo XC90",                                                                  // Название
  "stateData": {                                     
    "name": "Днепропетровск",                                                             // Город
    "regionName": "Днепропетровская",                                                     // Область
    "linkToCatalog": "/city/dnepropetrovsk/",
    "title": "Поиск объявлений по городу Днепропетровск",
    "stateId": 11                                                                         // id Города
  },
  "oldTop": {
    "isActive": true,
    "expireDate": ""
  },
  "canSetSpecificPhoneToAdvert": false,
  "dontComment": 0,
  "sendComments": 0,
  "badges": [
    
  ],
  "checkedVin": {                                                                        // Проверка vin-кода
    "isShow": false,                                                                     // Отображать vin-код
    "linkToReport": "/vin-check/auto/19050985/",
    "hasRestrictions": false,                                                            // Ограничения
    "checkDate": "04.05.2017",
    "isChecked": false                                                                  //  vin-код проверен
  },
  "isLeasing": 0,   // Лизинг 
  "dealer": {
    "link": "",
    "logo": "",
    "type": "",
    "id": 0,
    "name": "",
    "packageId": 0,
    "typeId": 0
  },
  "withInfoBar": false,                                                                // Информационная панель
  "infoBarText": "",
  "optionStyles": [
    
  ]    
]
 ```  
