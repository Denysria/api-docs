### Типы кузова

Типы кузова зависят от типов транспорта. Поэтому для того, чтобы получить список типов кузова необходимо отправить GET запрос на адрес `https://developers.ria.com/auto/categories/:categoryId/bodystyles?api_key=YOUR_API_KEY`, где *categoryId* - идентификатор типа транспорта, *api_key*- Ваш ключ.

Например, для легковых автомобилей ([https://developers.ria.com/auto/categories/1/bodystyles?api_key=YOUR_API_KEY](https://developers.ria.com/auto/categories/1/bodystyles?api_key=YOUR_API_KEY)), результат будет следующим:
```javascript
[
    { name: "Седан", value: 3 },
    { name: "Внедорожник / Кроссовер", value: 5 },
    { name: "Минивэн", value: 8 },
    { name: "Хэтчбек", value: 4 },
    { name: "Универсал", value: 2 },
    { name: "Купе", value: 6 },
    { name: "Легковой фургон (до 1,5 т)", value: 254 },
    { name: "Кабриолет", value: 7 },
    { name: "Пикап", value: 9 },
    { name: "Лимузин", value: 252 },
    { name: "Другой", value: 28 }
]
```

Также типы кузова могут быть разделены на группы. Это актуально для спецтехники. Поэтому существует способ получить сгруппированные типы кузова отправив GET запрос по адресу `https://developers.ria.com/auto/categories/:categoryId/bodystyles/_group?api_key=YOUR_API_KEY`, где *categoryId* - идентификатор типа транспорта, *api_key*- Ваш ключ.

Например, для мотоциклов ([https://developers.ria.com/auto/categories/2/bodystyles/_group?api_key=YOUR_API_KEY](https://developers.ria.com/auto/categories/2/bodystyles/_group?api_key=YOUR_API_KEY)), результат будет следующим:
```javascript
[
    [
        { name: "Мопеды", value: 58 },
        { name: "Скутер / Мотороллер", value: 11 },
        { name: "Макси-скутер", value: 12 }
    ],
    [
        { name: "Мотоциклы", value: 13 },
        { name: "Мотоцикл Без обтекателей (Naked bike)", value: 15 },
        { name: "Мотоцикл Внедорожный (Enduro)", value: 21 },
        { name: "Мотоцикл Кастом", value: 30 },
        { name: "Мотоцикл Классик", value: 14 },
        { name: "Мотоцикл Кросс", value: 19 },
        { name: "Мотоцикл Круизер", value: 24 },
        { name: "Мотоцикл Многоцелевой (All-round)", value: 25 },
        { name: "Мотоцикл с коляской", value: 29 },
        { name: "Спортбайк", value: 18 },
        { name: "Мотоцикл Спорт-туризм", value: 17 },
        { name: "Мотоцикл Супермото (Motard)", value: 22 },
        { name: "Мотоцикл Триал", value: 20 },
        { name: "Мотоцикл Туризм", value: 16 },
        { name: "Мотоцикл Чоппер", value: 23 }
    ],
    [
        { name: "Мини мотоциклы", value: 31 },
        { name: "Мини спорт", value: 32 },
        { name: "Мини крос (Питбайк)", value: 33 }
    ],
        { name: "Трицикл", value: 34 },
        { name: "Трайк", value: 57 },
    [
        { name: "Квадроциклы", value: 35 },
        { name: "Квадроцикл детский", value: 36 },
        { name: "Квадроцикл спортивный", value: 39 },
        { name: "Квадроцикл утилитарный", value: 41 },
        { name: "Мотовездеход", value: 42 },
        { name: "Вездеход-амфибия", value: 43 },
        { name: "Гольф-кар", value: 44 },
        { name: "Картинг", value: 45 }
    ],
    { name: "Снегоход", value: 46 },
    { name: "Другое", value: 56 }
]
```

Формат данных при этом отличается от обычного - это коллекция объектов, в которой есть другие коллекции. Группа типов кузовов всегда начинается с её названия. Например, в группу *Квадроциклы* входят типы кузовов *Квадроцикл детский*, *Квадроцикл спортивный*, *Квадроцикл утилитарный*, *Мотовездеход* и т.д.

Также, при необходимости, можно получиться просто весь список типов кузовов, послав GET запрос по адресу [https://developers.ria.com/auto/bodystyles?api_key=YOUR_API_KEY](https://developers.ria.com/auto/bodystyles?api_key=YOUR_API_KEY).
