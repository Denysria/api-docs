
Схема метода info
========

Метод возвращает данные про объявление по ID авто.
Что бы получить схему метода info с описанием полей

Запрос: 
````javascript
curl -XGET "https://auto.ria.com/graphql/schema/info?data=desc"
``
Что бы получить схему метода info с типами данных полей

Запрос: 
````javascript
curl -XGET "https://auto.ria.com/graphql/schema/info?data=type"
``

Запрос данных метод info
(Пока на тесте нужно передавать также куку -H "Cookie: testGraphQLGraphic=1")

**Метод info.**

Данные с одним агрументом id
Схема пользователю нужна для того что бы правильно сформировать запрос.
Запрос формируется исходя от данных которые нужны клиенту.
Например если нужны brand.id.
Исходя из схемы мы видим что в поле brand есть поле id. Пишем запрос...

Запрос: 
````javascript
curl -XPOST "https://auto.ria.com/graphql" -d '{"query":"{info(id:22587987){brand {id}}}"}' -H 'Content-Type: application/json' -H 'Cookie: testGraphQLGraphic=1'
``
как мы видим формат передаваемого объекта следующий:
````javascript
{
  "query":"{info(id:22587987){brand {id}}}"
}
``
давайте разберем строку query{info(id:22587987){brand {id}}}


info - название метода

id - [агрумент метода info] ID существующего объявления(в примере: 22587987)

{brand {id}} - запрашиваемые данные, клиент точно указывает, какие данные он хочет получить,
используя декларативную, графо-подобную структуру, которая очень напоминает формат JSON.


Ответ:
````javascript{
  "data": {
    "info": {
      "brand": {
        "id": "9"
      }
    }
  }
}
``
Если необходимо, к примеру, получить название и id бренда и название модели. Все останеться неизменным,
кроме запрашиваемых данных. Исходя со схеми запроса, они будут выглядеть так { brand {id name} model {name} },
а весь запрос так:

Запрос:
````javascript
curl -XPOST "https://auto.ria.com/graphql" -d '{"query":"{info(id:22587987){ brand {id name} model {name} }}"}' -H 'Content-Type: application/json' -H 'Cookie: testGraphQLGraphic=1'
``

Ответ:
````javascript
{
  "data": {
    "info": {
      "brand": {
        "id": "9",
        "name": "BMW"
      },
      "model": {
        "name": "X5"
      }
    }
  }
}
``
**Метод info.** 

Данные с двумя аргументами (id и userId)
Если в метод инфо передать еще один аргумент userId то в ответе мы можем запросить "частную" информацию о объявлении.
Такие как: история изменений (цены и описания), комментарии к объявлению.

Запрос: 
````javascript
curl -XPOST "https://auto.ria.com/graphql" -d '{"query":"{info(id:21519939, userId: 5820722){brand {id} changes {price {date newValue}}}}"}' -H 'Content-Type: application/json' -H 'Cookie: testGraphQLGraphic=1'
``
Пример запроса по изменению цены. Поля для запроса доступны в схеме.

Ответ:
````javascript
{
    "data":{
        "info":{
            "brand":{
                "id":"9"
            },
            "changes":{
                "price":[
                    {
                        "date":"2018-07-17 17:48:03",
                        "newValue":"5500"
                    },
                    {
                        "date":"2018-07-17 17:56:04",
                        "newValue":"6000"
                    },
                    {
                        "date":"2018-07-17 18:08:04",
                        "newValue":"5500"
                    },
                    {
                        "date":"2018-08-21 17:26:02",
                        "newValue":"5000"
                    }
                ]
            }
        }
    }
}
``
**Комментарии к объявлениям**

Запрос:
````javascript
curl -XPOST "https://auto.ria.com/graphql" -d '{"query":"{info(id: 21519939, userId: 5820722) {brand {id}wall{comments{permission propose {user{id} text date}}}}}"}' -H 'Content-Type: application/json' -H 'Cookie: testGraphQLGraphic=1'
``

info - метод
id - (агрумент 1) ID объявления
userId - (аргумент 2) ID юзера


Ответ:
``
{
  "data": {
    "info": {
      "brand": {
        "id": "9"
      },
      "wall": {
        "comments": {
          "permission": true,
          "propose": [
            {
              "user": {
                "id": "356384"
              },
              "text": "Комент1",
              "date": "2018-10-03T10:47:42.276Z"
            },
            {
              "user": {
                "id": "356384"
              },
              "text": "Комент2",
              "date": "2018-10-03T10:47:30.784Z"
            }
          ]
        }
      }
    }
  }
}
``
Графическая оболочка GraphQL
(Пока на тесте нужно засетапить куку **testGraphQLGraphic=1**)
