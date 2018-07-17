### Типы топлива

Типы топлива можно получить отправив GET запрос по адресу [https://developers.ria.com/auto/type?api_key=YOUR_API_KEY](https://developers.ria.com/auto/type?api_key=YOUR_API_KEY). Ответ будет выглядеть так:
```javascript
[
    { name: "Бензин", value: 1 },
    { name: "Дизель", value: 2 },
    { name: "Газ", value: 3 },
    { name: "Газ/бензин", value: 4 },
    { name: "Гибрид", value: 5 },
    { name: "Электро", value: 6 },
    { name: "Другое", value: 7 },
    { name: "Газ метан", value: 8 },
    { name: "Газ пропан-бутан", value: 9 }
]
```
