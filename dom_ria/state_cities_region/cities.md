### Города
  
  Города зависят от областей, поэтому, чтобы получить их список, необходимо послать GET запрос по адресу `https://developers.ria.com/dom/cities/:stateId?api_key=YOUR_API_KEY`, где *stateId* - идентификатор области.
  Для получение информации на украинском языке нужно добавить параметр *lang_id=4*
  
  Например, для Львовской области ([https://developers.ria.com/dom/cities/5?api_key=YOUR_API_KEY&lang_id=4](https://developers.ria.com/dom/cities/5?api_key=YOUR_API_KEY&lang_id=4) список городов будет следующим:
  
  ```json
 [
   {
     "lang_id": 4,
     "cityID": 287,
     "stateID": 5,
     "name": "Борислав",
     "eng": "borislav",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 288,
     "stateID": 5,
     "name": "Броди",
     "eng": "brodi",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 289,
     "stateID": 5,
     "name": "Буськ",
     "eng": "busk",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 290,
     "stateID": 5,
     "name": "Городок",
     "eng": "gorodok",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 291,
     "stateID": 5,
     "name": "Дрогобич",
     "eng": "drogobich",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 292,
     "stateID": 5,
     "name": "Жидачів",
     "eng": "jidachiv",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 293,
     "stateID": 5,
     "name": "Жовква",
     "eng": "jovkva",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 294,
     "stateID": 5,
     "name": "Золочев",
     "eng": "zolochev",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 295,
     "stateID": 5,
     "name": "Кам'янка-Бузька",
     "eng": "kam_yanka-buzka",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 5,
     "stateID": 5,
     "name": "Львів",
     "eng": "lviv",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 297,
     "stateID": 5,
     "name": "Миколаїв",
     "eng": "mikolayv",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 646,
     "stateID": 5,
     "name": "Моршин",
     "eng": "Morshun",
     "declension": null
   },
   {
     "lang_id": 4,
     "cityID": 298,
     "stateID": 5,
     "name": "Мостиська",
     "eng": "mostiska",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 632,
     "stateID": 5,
     "name": "Новий Розділ",
     "eng": "noviy-rozdil",
     "declension": "Новороздільский"
   },
   {
     "lang_id": 4,
     "cityID": 299,
     "stateID": 5,
     "name": "Перемишляни",
     "eng": "peremishlyani",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 300,
     "stateID": 5,
     "name": "Пустомити",
     "eng": "pustomiti",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 301,
     "stateID": 5,
     "name": "Радехів",
     "eng": "radehiv",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 302,
     "stateID": 5,
     "name": "Самбір",
     "eng": "sambir",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 303,
     "stateID": 5,
     "name": "Сколе",
     "eng": "skole",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 304,
     "stateID": 5,
     "name": "Сокаль",
     "eng": "sokal",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 614,
     "stateID": 5,
     "name": "Соснівка",
     "eng": "sosnovka",
     "declension": null
   },
   {
     "lang_id": 4,
     "cityID": 305,
     "stateID": 5,
     "name": "Старий Самбір",
     "eng": "stariyi_sambir",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 306,
     "stateID": 5,
     "name": "Стрий",
     "eng": "striyi",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 307,
     "stateID": 5,
     "name": "Трускавець",
     "eng": "truskavec",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 308,
     "stateID": 5,
     "name": "Турка",
     "eng": "turka",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 309,
     "stateID": 5,
     "name": "Червоноград",
     "eng": "chervonograd",
     "declension": ""
   },
   {
     "lang_id": 4,
     "cityID": 310,
     "stateID": 5,
     "name": "Яворів",
     "eng": "yavoriv",
     "declension": ""
   }
 ]
```  
