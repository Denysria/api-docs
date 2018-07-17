### Добавление обьявления

Чтобы добавить  объявления, Вам необходимо выполнить POST запрос такого вида:
````javascript
curl -X POST "https://developers.ria.com/auto/used/autos/?user_id=Ваш ID&api_key=YOUR_API_KEY" -H "accept: application/json" -H "content-type: application/json" -d "{ \  \ }"`
````
, где *user_id* - Ваш ID в системе RIA.com,  *`-d "{ \  \  }`* - здесь Вы указываете массив параметров которые хотите добавить,  *api_key* - Ваш ключ.

Объявления по умолчанию добавляются в черновики, чтобы опубликовать их, Вам нужно зайти в свой личный кабинет на AUTO.RIA

Также стоит заметить, что существуют параметры обязательны для заполнения. Детально с параметрами можно ознакомиться [здесь](#user-content-Структура-параметров).

**Пример запроса**

````javascript
curl -X POST "https://developers.ria.com/auto/used/autos/?user_id=7069830&api_key=YOUR_API_KEY" -H "accept: application/json" -H "content-type: application/json" -d "{ \"damage\": false, \"custom\": false, \"year\": 2016, \"price\": { \"value\": 80000, \"currency\": { \"id\": 1 } }, \"categories\": { \"main\": { \"id\": 1 } }, \"brand\": { \"id\": 5 }, \"model\": { \"id\": 963 }, \"modification\": \"V12 AMG B-turbo\", \"body\": { \"id\": 6 }, \"mileage\": 32, \"region\": { \"id\": 10 }, \"city\": { \"id\": 10 }, \"VIN\": \"JKBVNCB164A662141\", \"gearbox\": { \"id\": 1 }, \"drive\": { \"id\": 2 }, \"fuel\": { \"id\": 2, \"consumption\": { \"city\": 10, \"route\": 6, \"combine\": 8 } }, \"engine\": { \"volume\": { \"liters\": 3.5 } }, \"power\": { \"hp\": 585, \"kW\": 430 }, \"color\": { \"id\": 10, \"metallic\": true }, \"post\": { \"auctions\": true, \"comments\": { \"allowed\": true, \"check\": false }, \"exchanges\": { \"payment\": { \"id\": 2 }, \"type\": { \"id\": 1 } } }, \"video\": { \"key\": \"lLEiT9PeHSg\" }, \"description\": { \"ru\": \"Авто в идеальном состоянии, вложений не требует\", \"uk\": \"Авто в ідеальному стані, вкладень не потребує\" }, \"doors\": 2, \"seats\": 2, \"country\": { \"import\": { \"id\": 0 } }, \"spareParts\": false}"
`````
Развернутый пример

````json
curl -X POST "https://developers.ria.com/auto/used/autos/?user_id=7069830&api_key=YOUR_API_KEY" -H "accept: application/json" -H "content-type: application/json" -d
"{
   \"damage\":false,
   \"custom\":false,
   \"year\":2016,
   \"price\":{
      \"value\":80000,
      \"currency\":{
         \"id\":1
      }
   },
   \"categories\":{
      \"main\":{
         \"id\":1
      }
   },
   \"brand\":{
      \"id\":5
   },
   \"model\":{
      \"id\":963
   },
   \"modification\":\"V12 AMG B-turbo\",
   \"body\":{
      \"id\":6
   },
   \"mileage\":32,
   \"region\":{
      \"id\":10
   },
   \"city\":{
      \"id\":10
   },
   \"VIN\":\"JKBVNCB164A662141\",
   \"gearbox\":{
      \"id\":1
   },
   \"drive\":{
      \"id\":2
   },
   \"fuel\":{
      \"id\":2,
      \"consumption\":{
         \"city\":10,
         \"route\":6,
         \"combine\":8
      }
   },
   \"engine\":{
      \"volume\":{
         \"liters\":3.5
      }
   },
   \"power\":{
      \"hp\":585,
      \"kW\":430
   },
   \"color\":{
      \"id\":10,
      \"metallic\":true
   },
   \"post\":{
      \"auctions\":true,
      \"comments\":{
         \"allowed\":true,
         \"check\":false
      },
      \"exchanges\":{
         \"payment\":{
            \"id\":2
         },
         \"type\":{
            \"id\":1
         }
      }
   },
   \"video\":{
      \"key\":\"lLEiT9PeHSg\"
   },
   \"description\":{
      \"ru\":\"Авто в идеальном состоянии,
      вложений не требует\",
      \"uk\":\"Авто в ідеальному стані,
      вкладень не потребує\"
   },
   \"doors\":2,
   \"seats\":2,
   \"country\":{
      \"import\":{
         \"id\":0
      }
   },
   \"spareParts\":false
} "
````

**Пример успешного ответа:**

````json
{
   "damage":false,
   "custom":false,
   "year":2016,
   "price":{
      "value":80000,
      "currency":{
         "id":1
      }
   },
   "categories":{
      "main":{
         "id":1
      },
      "all":[
         {
            "id":1
         }
      ]
   },
   "brand":{
      "id":5
   },
   "model":{
      "id":963
   },
   "modification":"V12 AMG B-turbo",
   "body":{
      "id":6
   },
   "mileage":32,
   "region":{
      "id":10
   },
   "city":{
      "id":10
   },
   "VIN":"JKBVNCB164A66XXXX",
   "gearbox":{
      "id":1
   },
   "drive":{
      "id":2
   },
   "fuel":{
      "id":2,
      "consumption":{
         "city":10,
         "route":6,
         "combine":8
      }
   },
   "engine":{
      "volume":{
         "liters":3.5
      }
   },
   "power":{
      "hp":585,
      "kW":430
   },
   "color":{
      "id":10,
      "metallic":true
   },
   "post":{
      "auctions":true,
      "comments":{
         "allowed":true,
         "check":false
      },
      "exchanges":{
         "payment":{
            "id":2
         },
         "type":{
            "id":1
         }
      }
   },
   "video":{
      "key":"lLEiT9PeHSg"
   },
   "description":{
      "ru":"Авто в идеальном состоянии, вложений не требует",
      "uk":"Авто в ідеальному стані, вкладень не потребує"
   },
   "doors":2,
   "seats":2,
   "country":{
      "import":{
         "id":0
      }
   },
   "spareParts":false,
   "user":{
      "id":7069830
   },
   "ip":"80.91.174.90",
   "dates":{
      "created":"2017-09-18T12:07:43.840Z"
   },
   "status":{
      "id":13
   },
   "_id":20476120
}
````