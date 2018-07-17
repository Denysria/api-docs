### Города

Города зависят от областей, поэтому, чтобы получить их список, необходимо послать GET запрос по адресу `https://developers.ria.com/auto/states/:stateId/cities?api_key=YOUR_API_KEY`, где *stateId* - идентификатор области, *api_key*- Ваш ключ.

Например, для Винницкой области ([https://developers.ria.com/auto/states/1/cities?api_key=YOUR_API_KEY](https://developers.ria.com/auto/states/1/cities?api_key=YOUR_API_KEY)) список городов будет следующим:
```javascript
[
    { name: "Винница", value: 1 },
    { name: "Жмеринка", value: 27 },
    { name: "Казатин", value: 30 },
    { name: "Крыжополь", value: 31 },
    { name: "Липовец", value: 32 },
    { name: "Литин", value: 33 },
    { name: "Могилев-Подольский", value: 34 },
    { name: "Мурованые Куриловцы", value: 35 },
    { name: "Немиров", value: 36 },
    { name: "Оратов", value: 37 },
    { name: "Песчанка", value: 38 },
    { name: "Погребище", value: 39 },
    { name: "Теплик", value: 40 },
    { name: "Тывров", value: 41 },
    { name: "Томашполь", value: 42 },
    { name: "Тростянец", value: 43 },
    { name: "Тульчин", value: 44 },
    { name: "Хмельник", value: 45 },
    { name: "Черновцы", value: 46 },
    { name: "Чечельник", value: 47 },
    { name: "Шаргород", value: 48 },
    { name: "Ямполь", value: 49 },
    { name: "Бар", value: 597 },
    { name: "Бершадь", value: 599 },
    { name: "Гайсин", value: 602 },
    { name: "Ильинцы", value: 603 },
    { name: "Калиновка", value: 604 },
    { name: "Гнивань", value: 609 },
    { name: "Ладыжин", value: 644 }
]
```
