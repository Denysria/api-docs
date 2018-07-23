### Модели

Модели зависят от типов транспорта и марок. Следовательно список марок можно получить по адресу `http://api.auto.ria.com/auto/categories/:categoryId/marks/:markId/models?api_key=YOUR_API_KEY`, где *categoryId* - идентификатор типа транспорта а *markId* - идентификатор марки, *api_key*- Ваш ключ.

Например, для мотоциклов BMW ([https://developers.ria.com/auto/categories/2/marks/9/models?api_key=YOUR_API_KEY](https://developers.ria.com/auto/categories/2/marks/9/models?api_key=YOUR_API_KEY)), список моделей будет следующим:
```javascript
[
    { name: "Adventure", value: 25290 },
    { name: "C", value: 25291 },
    { name: "CS", value: 25292 },
    { name: "DKW", value: 28318 },
    { name: "F", value: 25293 },
    { name: "G", value: 29468 },
    { name: "GS", value: 25295 },
    { name: "HP", value: 38148 },
    { name: "Independent", value: 25297 },
    { name: "K", value: 25298 },
    { name: "LT", value: 25299 },
    { name: "R", value: 25300 },
    { name: "RS", value: 32736 },
    { name: "RT", value: 25301 },
    { name: "S", value: 25302 },
    { name: "X", value: 42030 }
]
```

Модели, также как и типы кузовов, могут быть сгруппированы. Чтобы получить такой список, необходимо отправить запрос по адресу `https://developers.ria.com/auto/categories/:categoryId/marks/:markId/models/_group?api_key=YOUR_API_KEY`, где *categoryId* - идентификатор типа транспорта а *markId* - идентификатор марки, *api_key*- Ваш ключ.

Например, для легковых автомобилей BMW ([https://developers.ria.com/auto/categories/1/marks/9/models/_group?api_key=YOUR_API_KEY](https://developers.ria.com/auto/categories/1/marks/9/models/_group?api_key=YOUR_API_KEY)), список моделей будет следующим:
```javascript
[
    [
        { name: "1 Series (все)", value: 2161 },
        { name: "116", value: 34670 },
        { name: "118", value: 34671 },
        { name: "120", value: 34672 },
        { name: "123", value: 34673 },
        { name: "125", value: 34674 },
        { name: "130", value: 34675 },
        { name: "135", value: 34676 }
    ],
    [
        { name: "3 Series (все)", value: 3219 },
        { name: "3 Series GT", value: 43029 },
        { name: "315", value: 37454 },
        { name: "316", value: 30851 },
        { name: "318", value: 31612 },
        { name: "320", value: 31611 },
        { name: "321", value: 37389 },
        { name: "323", value: 34677 },
        { name: "324", value: 30687 },
        { name: "325", value: 29713 },
        { name: "326", value: 44061 },
        { name: "328", value: 31661 },
        { name: "330", value: 34678 },
        { name: "335", value: 34679 },
        { name: "340", value: 35568 }
    ],
    ...
    { name: "Alpina", value: 906 },
    { name: "Dixi", value: 33383 },
    { name: "I3", value: 44838 },
    { name: "I8", value: 44537 },
    { name: "Isetta", value: 32380 },
    { name: "Z1", value: 97 },
    { name: "Z3", value: 98 },
    { name: "Z4", value: 99 },
    { name: "Z8", value: 100 }
]
```
Формат данных такой же как и в случае с типа кузова - коллекция объектов, в которой могут быть другие объекты. Группа моделей всегда начинается с её названия.

Также, при необходимости, можно просто получить список всех моделей, отправив GET запрос по адресу [https://developers.ria.com/auto/models?api_key=YOUR_API_KEY](https://developers.ria.com/auto/models?api_key=YOUR_API_KEY).
