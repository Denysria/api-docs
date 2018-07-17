### Районы

 Районы зависят от городов, поэтому, чтобы получить их список, необходимо послать GET запрос по адресу `https://developers.ria.com/dom/cities_districts/:city_id?api_key=YOUR_API_KEY`, где *city_id* - идентификатор города.
 Для получение информации на украинском языке нужно добавить параметр *lang_id=4*
  
Например, для города Львова ([https://developers.ria.com/dom/cities_districts/5?api_key=YOUR_API_KEY](https://developers.ria.com/dom/cities_districts/5?api_key=YOUR_API_KEY&) список районов будет следующим:
  
  ```json
  [
    [
      {
        "name": "Район",
        "value": ""
      },
      {
        "city_id": 5,
        "area_id": 15754,
        "name": "Аеропорт",
        "type": 1,
        "value": 15754
      },
      {
        "city_id": 5,
        "area_id": 15765,
        "name": "Арсен",
        "type": 1,
        "value": 15765
      },
      {
        "city_id": 5,
        "area_id": 15750,
        "name": "Білогорща",
        "type": 1,
        "value": 15750
      },
      {
        "city_id": 5,
        "area_id": 15771,
        "name": "Бондарівка",
        "type": 1,
        "value": 15771
      },
      {
        "city_id": 5,
        "area_id": 15751,
        "name": "Виговського",
        "type": 1,
        "value": 15751
      },
      {
        "city_id": 5,
        "area_id": 15763,
        "name": "Винники",
        "type": 1,
        "value": 15763
      },
      {
        "city_id": 5,
        "area_id": 15087,
        "name": "Галицький",
        "type": 1,
        "value": 15087
      },
      {
        "city_id": 5,
        "area_id": 15777,
        "name": "Голоско",
        "type": 1,
        "value": 15777
      },
      {
        "city_id": 5,
        "area_id": 15088,
        "name": "Залізничний",
        "type": 1,
        "value": 15088
      },
      {
        "city_id": 5,
        "area_id": 15778,
        "name": "Замарстинів",
        "type": 1,
        "value": 15778
      },
      {
        "city_id": 5,
        "area_id": 15779,
        "name": "Збоїща",
        "type": 1,
        "value": 15779
      },
      {
        "city_id": 5,
        "area_id": 15760,
        "name": "Знесення",
        "type": 1,
        "value": 15760
      },
      
      {
        "city_id": 5,
        "area_id": 15767,
        "name": "Новий Львів",
        "type": 1,
        "value": 15767
      },
      {
        "city_id": 5,
        "area_id": 15773,
        "name": "Новий Світ",
        "type": 1,
        "value": 15773
      },
      {
        "city_id": 5,
        "area_id": 15768,
        "name": "Пасіки",
        "type": 1,
        "value": 15768
      },
      {
        "city_id": 5,
        "area_id": 15772,
        "name": "Персеньківка",
        "type": 1,
        "value": 15772
      },
      {
        "city_id": 5,
        "area_id": 15769,
        "name": "Пироговка",
        "type": 1,
        "value": 15769
      },
      
      .......................
      
      
      {
        "city_id": 5,
        "area_id": 15775,
        "name": "Ринок Південний",
        "type": 1,
        "value": 15775
      },
      {
        "city_id": 5,
        "area_id": 15748,
        "name": "Рясне",
        "type": 1,
        "value": 15748
      },
      {
        "city_id": 5,
        "area_id": 15766,
        "name": "Санта Барбара",
        "type": 1,
        "value": 15766
      },
      {
        "city_id": 5,
        "area_id": 15753,
        "name": "Сигнівка",
        "type": 1,
        "value": 15753
      },
      {
        "city_id": 5,
        "area_id": 15090,
        "name": "Сихівський",
        "type": 1,
        "value": 15090
      },
      {
        "city_id": 5,
        "area_id": 15752,
        "name": "Скнилів",
        "type": 1,
        "value": 15752
      },
      {
        "city_id": 5,
        "area_id": 15747,
        "name": "Снопківська",
        "type": 1,
        "value": 15747
      },
      {
        "city_id": 5,
        "area_id": 15764,
        "name": "ТЦ Іскра",
        "type": 1,
        "value": 15764
      },
      {
        "city_id": 5,
        "area_id": 15091,
        "name": "Франківський",
        "type": 1,
        "value": 15091
      },
      {
        "city_id": 5,
        "area_id": 15745,
        "name": "Цитадель",
        "type": 1,
        "value": 15745
      },
      {
        "city_id": 5,
        "area_id": 15092,
        "name": "Шевченківський",
        "type": 1,
        "value": 15092
      }
    ],
    [
      {
        "name": "Пригород",
        "value": ""
      },
      {
        "city_id": 5,
        "area_id": 7494,
        "name": "Брюховичі",
        "type": 2,
        "value": 7494
      },
      {
        "city_id": 5,
        "area_id": 15742,
        "name": "Зимна Вода",
        "type": 2,
        "value": 15742
      },
      {
        "city_id": 5,
        "area_id": 15743,
        "name": "Малечковичі",
        "type": 2,
        "value": 15743
      },
      {
        "city_id": 5,
        "area_id": 15741,
        "name": "Сокільники",
        "type": 2,
        "value": 15741
      }
    ],
    [
      {
        "name": "Село",
        "value": ""
      },
      {
        "city_id": 5,
        "area_id": 7495,
        "name": "Винники",
        "type": 3,
        "value": 7495
      },
      {
        "city_id": 5,
        "area_id": 17513,
        "name": "Липники",
        "type": 3,
        "value": 17513
      },
      {
        "city_id": 5,
        "area_id": 7497,
        "name": "Рудне",
        "type": 3,
        "value": 7497
      }
    ]
  ]
  ```
