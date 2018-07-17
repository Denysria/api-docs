### Добавления фотографий к объявлению

Для добавления фотографий к объявлению, Вам необходимо выполнить POST запрос такого вида:

`curl -X POST "https://developers.ria.com/auto/used/autos/advertisementId/photos/upload?user_id=Ваш ID&api_key=YOUR API KEY" -H "accept: application/json" -H "content-type: application/json" -d "{ \"main\": \"главная фотография\", \"links\": [ \"фотографии" ]}"`

Расшифровка параметров:

- *advertisementId* - ID нужного Вам объявления
- *user_id* - Ваш ID в системе RIA.com
- *api_key* - Ваш ключ
- *`-d "{ \"main\": \"ссылка на главную фотографию\", \"links\": [ \"ссылки на фотографии" ]}"`* - здесь Вы указываете массив фотографий которые хотите добавить. В каждой ссылке на изображение должен присутствовать формат

Фотографии будут добавлены не по очередности, а в случайном порядке.

Полное описание сервиса "Добавления фотографий к объявлению" описаный с помощью стандарта **DeFacto swagger 2.0** [здесь](http://swagger.ria.com/ui/?api=auto/advertisements#/)

**Пример запроса**

`curl -X POST "https://developers.ria.com/auto/used/autos/21739303/photos/upload?user_id=7069830&api_key=bVjbA3izvnu04o7Pliw41bXAlY3mIj03CfQpeMNC" -H "accept: application/json" -H "content-type: application/json" -d "{ \"main\": \"https://cdn0.riastatic.com/photosnew/auto/photo/bmw_320__213471725fx.jpg\", \"links\": [ \"https://cdn0.riastatic.com/photosnew/auto/photo/bmw_320__213471725fx.jpg\", \"https://cdn0.riastatic.com/photosnew/auto/photo/bmw_320__213471726fx.jpg\" ]}"`

**Пример успешного ответа**

`{"message":"Ok","errors":[]}`
