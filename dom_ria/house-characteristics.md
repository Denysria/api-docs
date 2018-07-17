## Список характеристик недвижимости

Получить список областей можно отправив GET запрос по адресу [https://developers.ria.com/dom/options?category=id&realty_type=id&operation_type=id&api_key=YOUR_API_KEY](https://developers.ria.com/dom/options?category=id&realty_type=id&operation_type=id&api_key=YOUR_API_KEY).
, где 

- *category* - тип объекта

- *realty_type* - тип недвижимости

- *operation_type* - тип операции

или
````javascript
curl -X GET "https://developers.ria.com/dom/options?category=id&realty_type=id&operation_type=id&api_key=YOUR_API_KEY" -H "accept: application/json"
````

Для получение информации на украинском языке нужно добавить параметр *lang_id=4*

Полное описание сервиса "Список характеристик недвижимости" описанный с помощью стандарта DeFacto swagger 2.0 [здесь](http://swagger.ria.com/ui/?api=dom/options)

**Пример**

Допусти Вам нужно получить список характеристик объекта 'Дома', а тип недвижимости - 'Дачи', тип операции - 'Продажа'

Данный запрос будет выглядеть так:
````javascript
https://developers.ria.com/dom/options?category=4&realty_type=7&operation_type=1&api_key=YOUR_API_KEY
````
или 
````javascript
curl -X GET "https://developers.ria.com/dom/options?category=4&realty_type=7&operation_type=1&api_key=YOUR_API_KEY" -H "accept: application/json"
````
Результат будет следующим:
```json
[
  {
    "group_name": "комнаты",
    "group_prio": 150,
    "items": [
      {
        "characteristic_id": 209,
        "label": "комнат",
        "label_uk": "кімнат",
        "type_on_add": "text",
        "type_on_search": "text",
        "data_type": "int",
        "required": 1,
        "characteristic_category": "main",
        "prio": 150,
        "name": "Комнат",
        "group_name": "комнаты",
        "group_name_uk": "кімнати",
        "field_name": "rooms_count",
        "display_label_search": 0,
        "display_label_add": 0,
        "group_orientation_search": "horisontal",
        "group_orientation_add": "horisontal",
        "empty_value": 0,
        "type": "characteristic",
        "group_prio": 0
      }
    ]
  },
  {
    "group_name": "Тип стен",
    "group_prio": 100,
    "items": [
      {
        "characteristic_id": 149,
        "label": "тип стен",
        "label_uk": "тип стін",
        "type_on_add": "select",
        "type_on_search": "checkbox",
        "data_type": "int",
        "required": 1,
        "characteristic_category": "main",
        "prio": 100,
        "name": "тип стен для дома",
        "group_name": "Тип стен",
        "group_name_uk": "Тип стін",
        "children": {
          "129": {
            "characteristic_id": "129",
            "name": "кирпич",
            "name_uk": "цегла",
            "prio": "200"
          },
          "130": {
            "characteristic_id": "130",
            "name": "кирпич силикатный",
            "name_uk": "цегла силікатна",
            "prio": "190"
          },
          "131": {
            "characteristic_id": "131",
            "name": "кирпич саманный",
            "name_uk": "цегла саманна",
            "prio": "180"
          },
          "132": {
            "characteristic_id": "132",
            "name": "дерево и кирпич",
            "name_uk": "дерево та цегла",
            "prio": "170"
          },
          "133": {
            "characteristic_id": "133",
            "name": "панель",
            "name_uk": "панель",
            "prio": "160"
          },
          "134": {
            "characteristic_id": "134",
            "name": "пеноблок",
            "name_uk": "пеноблок",
            "prio": "150"
          },
          "135": {
            "characteristic_id": "135",
            "name": "керамзитобетон",
            "name_uk": "керамзітобетон",
            "prio": "140"
          },
          "136": {
            "characteristic_id": "136",
            "name": "монолит",
            "name_uk": "моноліт",
            "prio": "130"
          },
          "138": {
            "characteristic_id": "138",
            "name": "сруб",
            "name_uk": "зруб",
            "prio": "110"
          },
          "139": {
            "characteristic_id": "139",
            "name": "брус",
            "name_uk": "брус",
            "prio": "100"
          },
          "140": {
            "characteristic_id": "140",
            "name": "каркасно-щитовой",
            "name_uk": "каркасно-щитовий",
            "prio": "90"
          },
          "141": {
            "characteristic_id": "141",
            "name": "глинобитный",
            "name_uk": "глинобитний",
            "prio": "80"
          },
          "142": {
            "characteristic_id": "142",
            "name": "пенобетон",
            "name_uk": "пінобетон",
            "prio": "70"
          },
          "143": {
            "characteristic_id": "143",
            "name": "газобетон",
            "name_uk": "газобетон",
            "prio": "60"
          },
          "144": {
            "characteristic_id": "144",
            "name": "сендвич-панели",
            "name_uk": "сендвіч-панелі",
            "prio": "50"
          },
          "145": {
            "characteristic_id": "145",
            "name": "метал",
            "name_uk": "метал",
            "prio": "40"
          },
          "146": {
            "characteristic_id": "146",
            "name": "поротерм",
            "name_uk": "поротерм",
            "prio": "30"
          },
          "147": {
            "characteristic_id": "147",
            "name": "ракушечник (ракушняк)",
            "name_uk": "ракушняк",
            "prio": "20"
          },
          "148": {
            "characteristic_id": "148",
            "name": "инкерманский камень",
            "name_uk": "інкерманський камінь",
            "prio": "10"
          },
          "1433": {
            "characteristic_id": "1433",
            "name": "шлакобетон",
            "name_uk": "шлакобетон",
            "prio": "65"
          },
          "1441": {
            "characteristic_id": "1441",
            "name": "шлакоблок",
            "name_uk": "шлакоблок",
            "prio": "55"
          },
          "1442": {
            "characteristic_id": "1442",
            "name": "наливной",
            "name_uk": "наливний",
            "prio": "5"
          },
          "1444": {
            "characteristic_id": "1444",
            "name": "бутовый камень",
            "name_uk": "бутовий камінь",
            "prio": "4"
          },
          "1445": {
            "characteristic_id": "1445",
            "name": "мергель",
            "name_uk": "мергель",
            "prio": "3"
          },
          "1447": {
            "characteristic_id": "1447",
            "name": "крупноблочный известняк",
            "name_uk": "великоблочний вапняк",
            "prio": "2"
          },
          "1463": {
            "characteristic_id": "1463",
            "name": "термоблок",
            "name_uk": "термоблок",
            "prio": "1"
          },
          "1597": {
            "characteristic_id": "1597",
            "name": "сип панель ",
            "name_uk": "сіп панель",
            "prio": "56"
          },
          "1598": {
            "characteristic_id": "1598",
            "name": "контейнер ",
            "name_uk": "контейнер",
            "prio": "7"
          }
        },
        "field_name": "wall_type",
        "display_label_search": 0,
        "display_label_add": 0,
        "group_orientation_search": "horisontal",
        "group_orientation_add": "horisontal",
        "empty_value": 0,
        "type": "characteristic",
        "group_prio": 0
      }
    ]
  },
  {
    "group_name": "площадь помещений",
    "group_prio": 90,
    "items": [
      {
        "characteristic_id": 215,
        "label": "общая пл.",
        "label_uk": "загальна пл.",
        "type_on_add": "text",
        "type_on_search": "text",
        "data_type": "float",
        "required": 1,
        "sufix": "м.кв.",
        "characteristic_category": "main",
        "prio": 4,
        "name": "площадь дома",
        "group_name": "площадь помещений",
        "group_name_uk": "площа приміщень",
        "group_prio": 90,
        "field_name": "total_square_meters",
        "display_label_search": 0,
        "display_label_add": 0,
        "group_orientation_search": "horisontal",
        "group_orientation_add": "horisontal",
        "empty_value": 0,
        "type": "characteristic"
      },
      {
        "characteristic_id": 216,
        "label": "жилая",
        "label_uk": "житлова",
        "type_on_add": "text",
        "type_on_search": "text",
        "data_type": "float",
        "required": 0,
        "sufix": "кв. м",
        "characteristic_category": "main",
        "prio": 3,
        "name": "жилая площадь",
        "group_name": "площадь помещений",
        "group_name_uk": "площа приміщень",
        "group_prio": 90,
        "field_name": "living_square_meters",
        "display_label_search": 0,
        "display_label_add": 0,
        "group_orientation_search": "horisontal",
        "group_orientation_add": "horisontal",
        "empty_value": 0,
        "type": "characteristic"
      },
      {
        "characteristic_id": 218,
        "label": "кухня",
        "label_uk": "кухня",
        "type_on_add": "text",
        "type_on_search": "text",
        "data_type": "float",
        "required": 0,
        "sufix": "кв. м",
        "characteristic_category": "main",
        "prio": 2,
        "name": "кухня",
        "group_name": "площадь помещений",
        "group_name_uk": "площа приміщень",
        "group_prio": 90,
        "field_name": "kitchen_square_meters",
        "display_label_search": 0,
        "display_label_add": 0,
        "group_orientation_search": "horisontal",
        "group_orientation_add": "horisontal",
        "empty_value": 0,
        "type": "characteristic"
      }
    ]
  },
  {
    "group_name": "площадь участка",
    "group_prio": 83,
    "items": [
      {
        "characteristic_id": 219,
        "label": "участок",
        "label_uk": "ділянка",
        "type_on_add": "text",
        "type_on_search": "text",
        "data_type": "float",
        "required": 0,
        "characteristic_category": "main",
        "prio": 10,
        "name": "площадь участка",
        "group_name": "площадь участка",
        "group_name_uk": "площа ділянки",
        "group_prio": 85,
        "field_name": "ares_count",
        "display_label_search": 0,
        "display_label_add": 0,
        "group_orientation_search": "horisontal",
        "group_orientation_add": "horisontal",
        "empty_value": 0,
        "type": "characteristic"
      },
      {
        "characteristic_id": 226,
        "label": "единица измерения",
        "label_uk": "одиниця виміру",
        "type_on_add": "select",
        "type_on_search": "select",
        "data_type": "int",
        "required": 0,
        "characteristic_category": "main",
        "prio": 2,
        "name": "единица измерения площади участка",
        "group_name": "площадь участка",
        "group_name_uk": "площа ділянки",
        "group_prio": 83,
        "children": {
          "223": {
            "characteristic_id": "223",
            "name": "сотка",
            "name_uk": "сотка",
            "prio": "3"
          },
          "224": {
            "characteristic_id": "224",
            "name": "Га (гектар)",
            "name_uk": "Га (гектар)",
            "prio": "2"
          },
          "225": {
            "characteristic_id": "225",
            "name": "кв. м",
            "name_uk": "кв. м",
            "prio": "1"
          }
        },
        "field_name": "lot_unit",
        "display_label_search": 0,
        "display_label_add": 0,
        "group_orientation_search": "horisontal",
        "group_orientation_add": "horisontal",
        "empty_value": 0,
        "type": "characteristic"
      }
    ]
  },
  {
    "group_name": "этаж",
    "group_prio": 75,
    "items": [
      {
        "characteristic_id": 1494,
        "label": "у озера",
        "label_uk": "біля озера",
        "type_on_add": "checkbox",
        "type_on_search": "checkbox",
        "data_type": "int",
        "required": 0,
        "characteristic_category": "main",
        "prio": 4,
        "name": "у озера",
        "group_name": "этаж",
        "group_name_uk": "поверх",
        "group_prio": 75,
        "display_label_search": 1,
        "display_label_add": 1,
        "group_orientation_search": "horisontal",
        "group_orientation_add": "horisontal",
        "empty_value": 0,
        "type": "characteristic"
      },
      {
        "characteristic_id": 1493,
        "label": "у реки",
        "label_uk": "біля річки",
        "type_on_add": "checkbox",
        "type_on_search": "checkbox",
        "data_type": "int",
        "required": 0,
        "characteristic_category": "main",
        "prio": 3,
        "name": "у реки",
        "group_name": "этаж",
        "group_name_uk": "поверх",
        "group_prio": 75,
        "display_label_search": 1,
        "display_label_add": 1,
        "group_orientation_search": "horisontal",
        "group_orientation_add": "horisontal",
        "empty_value": 0,
        "type": "characteristic"
      },
      {
        "characteristic_id": 230,
        "label": "мансардный этаж",
        "label_uk": "мансардний поверх",
        "type_on_add": "checkbox",
        "type_on_search": "checkbox",
        "data_type": "int",
        "required": 0,
        "characteristic_category": "main",
        "prio": 2,
        "name": "мансардный этаж",
        "group_name": "этаж",
        "group_name_uk": "поверх",
        "group_prio": 75,
        "display_label_search": 0,
        "display_label_add": 0,
        "group_orientation_search": "horisontal",
        "group_orientation_add": "horisontal",
        "empty_value": 0,
        "type": "characteristic"
      },
      {
        "characteristic_id": 231,
        "label": "подвальный / цокольный этаж",
        "label_uk": "підвальний / цокольний поверх",
        "type_on_add": "checkbox",
        "type_on_search": "checkbox",
        "data_type": "int",
        "required": 0,
        "characteristic_category": "main",
        "prio": 1,
        "name": "подвальный / цокольный этаж",
        "group_name": "этаж",
        "group_name_uk": "поверх",
        "group_prio": 75,
        "display_label_search": 0,
        "display_label_add": 0,
        "group_orientation_search": "horisontal",
        "group_orientation_add": "horisontal",
        "empty_value": 0,
        "type": "characteristic"
      }
    ]
  },
  {
    "group_name": "характеристика здания",
    "group_prio": 70,
    "items": [
      {
        "characteristic_id": 443,
        "label": "год постройки",
        "label_uk": "рік побудови",
        "type_on_add": "select",
        "type_on_search": "checkbox",
        "data_type": "int",
        "required": 0,
        "default_value": "не указано",
        "characteristic_category": "main",
        "prio": 160,
        "name": "год постройки",
        "group_name": "характеристика здания",
        "group_name_uk": "характеристика будівлі",
        "group_prio": 70,
        "children": {
          "421": {
            "characteristic_id": "421",
            "name": "2015, IV кв.",
            "name_uk": "2015, IV кв.",
            "prio": "25"
          },
          "422": {
            "characteristic_id": "422",
            "name": "2013",
            "name_uk": "2013",
            "prio": "20"
          },
          "423": {
            "characteristic_id": "423",
            "name": "2012",
            "name_uk": "2012",
            "prio": "19"
          },
          "424": {
            "characteristic_id": "424",
            "name": "2011 ",
            "name_uk": "2011",
            "prio": "18"
          },
          "425": {
            "characteristic_id": "425",
            "name": "2010",
            "name_uk": "2010",
            "prio": "17"
          },
          "426": {
            "characteristic_id": "426",
            "name": "2009",
            "name_uk": "2009",
            "prio": "16"
          },
          "427": {
            "characteristic_id": "427",
            "name": "2008",
            "name_uk": "2008",
            "prio": "15"
          },
          "428": {
            "characteristic_id": "428",
            "name": "2007",
            "name_uk": "2007",
            "prio": "14"
          },
          "429": {
            "characteristic_id": "429",
            "name": "2006",
            "name_uk": "2006",
            "prio": "13"
          },
          "434": {
            "characteristic_id": "434",
            "name": "2001-2005",
            "name_uk": "2001-2005",
            "prio": "8"
          },
          "435": {
            "characteristic_id": "435",
            "name": "1990-2000",
            "name_uk": "1990-2000",
            "prio": "7"
          },
          "436": {
            "characteristic_id": "436",
            "name": "1980-1989",
            "name_uk": "1980-1989",
            "prio": "6"
          },
          "437": {
            "characteristic_id": "437",
            "name": "1970-1979",
            "name_uk": "1970-1979",
            "prio": "5"
          },
          "438": {
            "characteristic_id": "438",
            "name": "1960-1969",
            "name_uk": "1960-1969",
            "prio": "4"
          },
          "439": {
            "characteristic_id": "439",
            "name": "1944-1959",
            "name_uk": "1944-1959",
            "prio": "3"
          },
          "440": {
            "characteristic_id": "440",
            "name": "1917-1942",
            "name_uk": "1917-1942",
            "prio": "2"
          },
          "441": {
            "characteristic_id": "441",
            "name": "раньше 1917",
            "name_uk": "до 1917",
            "prio": "1"
          },
          "442": {
            "characteristic_id": "442",
            "name": "не указано",
            "name_uk": "не вказано",
            "prio": "36"
          },
          "1448": {
            "characteristic_id": "1448",
            "name": "2014",
            "name_uk": "2014",
            "prio": "21"
          },
          "1449": {
            "characteristic_id": "1449",
            "name": "Сдача в 2015",
            "name_uk": "Здача в 2015",
            "prio": "30"
          },
          "1450": {
            "characteristic_id": "1450",
            "name": "Сдача в 2016",
            "name_uk": "Здача в 2016",
            "prio": "31"
          },
          "1454": {
            "characteristic_id": "1454",
            "name": "2015, III кв.",
            "name_uk": "2015, III кв.",
            "prio": "24"
          },
          "1455": {
            "characteristic_id": "1455",
            "name": "2015, II кв.",
            "name_uk": "2015, II кв.",
            "prio": "23"
          },
          "1456": {
            "characteristic_id": "1456",
            "name": "2015, I кв.",
            "name_uk": "2015, I кв.",
            "prio": "22"
          },
          "1457": {
            "characteristic_id": "1457",
            "name": "2016, I кв.",
            "name_uk": "2016, I кв.",
            "prio": "26"
          },
          "1458": {
            "characteristic_id": "1458",
            "name": "2016, II кв.",
            "name_uk": "2016, II кв.",
            "prio": "27"
          },
          "1459": {
            "characteristic_id": "1459",
            "name": "2016, III кв.",
            "name_uk": "2016, III кв.",
            "prio": "28"
          },
          "1460": {
            "characteristic_id": "1460",
            "name": "2016, IV кв.",
            "name_uk": "2016, IV кв.",
            "prio": "29"
          },
          "1468": {
            "characteristic_id": "1468",
            "name": "Сдача в 2017",
            "name_uk": "Здача в 2017",
            "prio": "32"
          },
          "1469": {
            "characteristic_id": "1469",
            "name": "Сдача в 2018",
            "name_uk": "Здача в 2018",
            "prio": "33"
          },
          "1470": {
            "characteristic_id": "1470",
            "name": "Сдача в 2019",
            "name_uk": "Здача в 2019",
            "prio": "34"
          },
          "1471": {
            "characteristic_id": "1471",
            "name": "Сдача в 2020",
            "name_uk": "Здача в 2020",
            "prio": "35"
          }
        },
        "display_label_search": 0,
        "display_label_add": 0,
        "group_orientation_search": "horisontal",
        "group_orientation_add": "horisontal",
        "empty_value": 0,
        "type": "characteristic"
      }
    ]
  },
  {
    "group_name": "цена",
    "group_prio": 45,
    "items": [
      {
        "characteristic_id": 234,
        "label": "цена",
        "label_uk": "ціна",
        "type_on_add": "text",
        "type_on_search": "text",
        "data_type": "int",
        "required": 1,
        "characteristic_category": "main",
        "prio": 96,
        "name": "цена",
        "group_name": "цена",
        "group_name_uk": "ціна",
        "group_prio": 64,
        "field_name": "price",
        "display_label_search": 0,
        "display_label_add": 0,
        "group_orientation_search": "horisontal",
        "group_orientation_add": "horisontal",
        "empty_value": 0,
        "type": "characteristic"
      },
      {
        "characteristic_id": 1011,
        "label": "цена договорная",
        "label_uk": "ціна договірна",
        "type_on_add": "checkbox",
        "type_on_search": "checkbox",
        "data_type": "int",
        "required": 0,
        "characteristic_category": "main",
        "prio": 95,
        "name": "цена договорная",
        "group_name": "цена",
        "group_name_uk": "ціна",
        "group_prio": 64,
        "field_name": "is_negotiable",
        "display_label_search": 0,
        "display_label_add": 0,
        "group_orientation_search": "horisontal",
        "group_orientation_add": "horisontal",
        "empty_value": 0,
        "type": "characteristic"
      },
      {
        "characteristic_id": 242,
        "label": "тип валюты",
        "label_uk": "тип валюти",
        "type_on_add": "select",
        "type_on_search": "select",
        "data_type": "int",
        "required": 1,
        "default_value": "$",
        "characteristic_category": "main",
        "prio": 85,
        "name": "тип валюты (USD)",
        "group_name": "цена",
        "group_name_uk": "ціна",
        "group_prio": 64,
        "children": {
          "239": {
            "characteristic_id": "239",
            "name": "$",
            "name_uk": "$",
            "prio": "3"
          },
          "240": {
            "characteristic_id": "240",
            "name": "грн",
            "name_uk": "грн",
            "prio": "2"
          },
          "241": {
            "characteristic_id": "241",
            "name": "€",
            "name_uk": "€",
            "prio": "1"
          }
        },
        "field_name": "currency_type",
        "display_label_search": 0,
        "display_label_add": 0,
        "group_orientation_search": "horisontal",
        "group_orientation_add": "horisontal",
        "empty_value": 0,
        "type": "characteristic"
      },
      {
        "characteristic_id": 1464,
        "label": "стартовая цена",
        "label_uk": "стартова ціна",
        "type_on_add": "checkbox",
        "type_on_search": "checkbox",
        "data_type": "int",
        "required": 0,
        "characteristic_category": "main",
        "prio": 45,
        "name": "стартовая цена",
        "group_name": "цена",
        "group_name_uk": "ціна",
        "field_name": "start_price",
        "display_label_search": 0,
        "display_label_add": 0,
        "group_orientation_search": "horisontal",
        "group_orientation_add": "horisontal",
        "empty_value": 0,
        "type": "characteristic",
        "group_prio": 0
      },
      {
        "characteristic_id": 273,
        "label": "возможен торг",
        "label_uk": "можливий торг",
        "type_on_add": "checkbox",
        "type_on_search": "checkbox",
        "data_type": "int",
        "required": 0,
        "characteristic_category": "main",
        "prio": 42,
        "name": "возможен торг",
        "group_name": "цена",
        "group_name_uk": "ціна",
        "field_name": "is_bargain",
        "display_label_search": 0,
        "display_label_add": 0,
        "group_orientation_search": "horisontal",
        "group_orientation_add": "horisontal",
        "empty_value": 0,
        "type": "characteristic",
        "group_prio": 0
      },
      {
        "characteristic_id": 274,
        "label": "возможна рассрочка / кредит",
        "label_uk": "можлива розстрочка / кредит",
        "type_on_add": "checkbox",
        "type_on_search": "checkbox",
        "data_type": "int",
        "required": 0,
        "characteristic_category": "main",
        "prio": 40,
        "name": "возможна рассрочка / кредит",
        "group_name": "цена",
        "group_name_uk": "ціна",
        "display_label_search": 0,
        "display_label_add": 0,
        "group_orientation_search": "horisontal",
        "group_orientation_add": "horisontal",
        "empty_value": 0,
        "type": "characteristic",
        "group_prio": 0
      },
      {
        "characteristic_id": 265,
        "label": "возможен обмен",
        "label_uk": "можливий обмін",
        "type_on_add": "select",
        "type_on_search": "select",
        "data_type": "int",
        "required": 0,
        "default_value": "нет",
        "characteristic_category": "main",
        "prio": 35,
        "name": "возможен обмен",
        "group_name": "цена",
        "group_name_uk": "ціна",
        "children": {
          "257": {
            "characteristic_id": "257",
            "name": "нет",
            "name_uk": "ні",
            "prio": "8"
          },
          "258": {
            "characteristic_id": "258",
            "name": "на авто + моя доплата",
            "name_uk": "на авто + моя доплата",
            "prio": "7"
          },
          "259": {
            "characteristic_id": "259",
            "name": "на авто без доплаты",
            "name_uk": "на авто без доплати",
            "prio": "6"
          },
          "260": {
            "characteristic_id": "260",
            "name": "на авто + ваша доплата",
            "name_uk": "на авто + ваша доплата",
            "prio": "5"
          },
          "261": {
            "characteristic_id": "261",
            "name": "на недвижимость + моя доплата",
            "name_uk": "на нерухомість + моя доплата",
            "prio": "4"
          },
          "262": {
            "characteristic_id": "262",
            "name": "на недвижимость без доплаты",
            "name_uk": "на нерухомість без доплати",
            "prio": "3"
          },
          "263": {
            "characteristic_id": "263",
            "name": "на недвижимость + ваша доплата",
            "name_uk": "на нерухомість + ваша доплата",
            "prio": "2"
          },
          "264": {
            "characteristic_id": "264",
            "name": "рассмотрю любой вариант",
            "name_uk": "розгляну будь-який варіант",
            "prio": "1"
          }
        },
        "field_name": "is_exchange",
        "display_label_search": 0,
        "display_label_add": 0,
        "group_orientation_search": "horisontal",
        "group_orientation_add": "horisontal",
        "empty_value": 0,
        "type": "characteristic",
        "group_prio": 0
      },
      {
        "characteristic_id": 1437,
        "label": "тип предложения",
        "label_uk": "тип пропозиції",
        "type_on_add": "select",
        "type_on_search": "checkbox",
        "data_type": "int",
        "required": 0,
        "default_value": "от посредника",
        "characteristic_category": "main",
        "prio": 30,
        "name": "тип предложения",
        "group_name": "цена",
        "group_name_uk": "ціна",
        "group_prio": 64,
        "children": {
          "1434": {
            "characteristic_id": "1434",
            "name": "от посредника",
            "name_uk": "від посередника",
            "prio": "5"
          },
          "1435": {
            "characteristic_id": "1435",
            "name": "от представителя хозяина (без комиссионных)",
            "name_uk": "від представника власника (без комісійних)",
            "prio": "4"
          },
          "1436": {
            "characteristic_id": "1436",
            "name": "от собственника",
            "name_uk": "від власника",
            "prio": "2"
          },
          "1473": {
            "characteristic_id": "1473",
            "name": "от представителя застройщика",
            "name_uk": "від представника забудовника",
            "prio": "3"
          },
          "1506": {
            "characteristic_id": "1506",
            "name": "от застройщика",
            "name_uk": "від забудовника",
            "prio": "1"
          }
        },
        "display_label_search": 1,
        "display_label_add": 1,
        "group_orientation_search": "horisontal",
        "group_orientation_add": "horisontal",
        "empty_value": 0,
        "type": "characteristic"
      }
    ]
  }
]
```
