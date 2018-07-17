### Области
Получить список областей можно отправив GET запрос по адресу [https://developers.ria.com/dom/states?api_key=YOUR_API_KEY](https://developers.ria.com/dom/states?api_key=YOUR_API_KEY).
Для получение информации на украинском языке нужно добавить параметр *lang_id=4*

Полное описание сервиса "Методы для работы с областями, городами, районами" описанный с помощью стандарта DeFacto swagger 2.0 [здесь](http://swagger.ria.com/ui/?api=dom/states_cities_and_districts)

Результат будет следующим:
```json
[
  {
    "lang_id": 2,
    "stateID": 1,
    "name": "Винницкая",
    "eng_name": "vinnica",
    "declension": "Винницкой области",
    "center_declension": "Винницы",
    "region_name": "Винница"
  },
  {
    "lang_id": 2,
    "stateID": 18,
    "name": "Волынская",
    "eng_name": "luck",
    "declension": "Волынской области",
    "center_declension": "Луцка",
    "region_name": "Луцк"
  },
  {
    "lang_id": 2,
    "stateID": 11,
    "name": "Днепропетровская",
    "eng_name": "dnepropetrovsk",
    "declension": "Днепропетровской области",
    "center_declension": "Днепропетровска",
    "region_name": "Днепропетровск"
  },
  {
    "lang_id": 2,
    "stateID": 13,
    "name": "Донецкая",
    "eng_name": "doneck",
    "declension": "Донецкой области",
    "center_declension": "Донецка",
    "region_name": "Донецк"
  },
  {
    "lang_id": 2,
    "stateID": 2,
    "name": "Житомирская",
    "eng_name": "jitomir",
    "declension": "Житомирской области",
    "center_declension": "Житомира",
    "region_name": "Житомир"
  },
  {
    "lang_id": 2,
    "stateID": 22,
    "name": "Закарпатская",
    "eng_name": "ujgorod",
    "declension": "Закарпатской области",
    "center_declension": "Ужгорода",
    "region_name": "Ужгород"
  },
  {
    "lang_id": 2,
    "stateID": 14,
    "name": "Запорожская",
    "eng_name": "zaporoje",
    "declension": "Запорожской области",
    "center_declension": "Запорожья",
    "region_name": "Запорожье"
  },
  {
    "lang_id": 2,
    "stateID": 15,
    "name": "Ивано-Франковская",
    "eng_name": "ivano-frankovsk",
    "declension": "Ивано-Франковской области",
    "center_declension": "Ивано-Франковска",
    "region_name": "Ивано-Франковск"
  },
  {
    "lang_id": 2,
    "stateID": 10,
    "name": "Киевская",
    "eng_name": "kiev",
    "declension": "Киевской области",
    "center_declension": "Киева",
    "region_name": "Киев"
  },
  {
    "lang_id": 2,
    "stateID": 16,
    "name": "Кировоградская",
    "eng_name": "kirovograd",
    "declension": "Кировоградской области",
    "center_declension": "Кировограда",
    "region_name": "Кировоград"
  },
  {
    "lang_id": 2,
    "stateID": 17,
    "name": "Луганская",
    "eng_name": "lugansk",
    "declension": "Луганской области",
    "center_declension": "Луганска",
    "region_name": "Луганск"
  },
  {
    "lang_id": 2,
    "stateID": 5,
    "name": "Львовская",
    "eng_name": "lvov",
    "declension": "Львовской области",
    "center_declension": "Львова",
    "region_name": "Львов"
  },
  {
    "lang_id": 2,
    "stateID": 19,
    "name": "Николаевская",
    "eng_name": "nikolaev",
    "declension": "Николаевской области",
    "center_declension": "Николаева",
    "region_name": "Николаев"
  },
  {
    "lang_id": 2,
    "stateID": 12,
    "name": "Одесская",
    "eng_name": "odessa",
    "declension": "Одесской области",
    "center_declension": "Одессы",
    "region_name": "Одесса"
  },
  {
    "lang_id": 2,
    "stateID": 20,
    "name": "Полтавская",
    "eng_name": "poltava",
    "declension": "Полтавской области",
    "center_declension": "Полтавы",
    "region_name": "Полтава"
  },
  {
    "lang_id": 2,
    "stateID": 21,
    "name": "Республика Крым",
    "eng_name": "simferopol",
    "declension": "Республики Крым",
    "center_declension": "Симферополя",
    "region_name": "Республика Крым"
  },
  {
    "lang_id": 2,
    "stateID": 9,
    "name": "Ровенская",
    "eng_name": "rovno",
    "declension": "Ровенской области",
    "center_declension": "Ровно",
    "region_name": "Ровно"
  },
  {
    "lang_id": 2,
    "stateID": 8,
    "name": "Сумская",
    "eng_name": "sumiy",
    "declension": "Сумской области",
    "center_declension": "Сум",
    "region_name": "Сумы"
  },
  {
    "lang_id": 2,
    "stateID": 3,
    "name": "Тернопольская",
    "eng_name": "ternopol",
    "declension": "Тернопольской области",
    "center_declension": "Тернополя",
    "region_name": "Тернополь"
  },
  {
    "lang_id": 2,
    "stateID": 7,
    "name": "Харьковская",
    "eng_name": "harkov",
    "declension": "Харьковской области",
    "center_declension": "Харькова",
    "region_name": "Харьков"
  },
  {
    "lang_id": 2,
    "stateID": 23,
    "name": "Херсонская",
    "eng_name": "herson",
    "declension": "Херсонской области",
    "center_declension": "Херсона",
    "region_name": "Херсон"
  },
  {
    "lang_id": 2,
    "stateID": 4,
    "name": "Хмельницкая",
    "eng_name": "hmelnickiy",
    "declension": "Хмельницкой области",
    "center_declension": "Хмельницкого",
    "region_name": "Хмельницкий"
  },
  {
    "lang_id": 2,
    "stateID": 24,
    "name": "Черкасская",
    "eng_name": "cherkassiy",
    "declension": "Черкасской области",
    "center_declension": "Черкасс",
    "region_name": "Черкассы"
  },
  {
    "lang_id": 2,
    "stateID": 6,
    "name": "Черниговская",
    "eng_name": "chernigov",
    "declension": "Черниговской области",
    "center_declension": "Чернигова",
    "region_name": "Чернигов"
  },
  {
    "lang_id": 2,
    "stateID": 25,
    "name": "Черновицкая",
    "eng_name": "chernovciy",
    "declension": "Черновицкой области",
    "center_declension": "Черновцов",
    "region_name": "Черновцы"
  }
