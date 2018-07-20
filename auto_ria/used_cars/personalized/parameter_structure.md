
### Структура параметров


**Параметры которые должны обязательно присутствовать в запросе**


<table>

<thead>

<tr>

<th align="left">Имя поля</th>

<th align="left">Тип</th>

<th align="left">Описание</th>

<th align="left">Пример</th>

</tr>

</thead>

<tbody>

<tr>

<td align="left">* year</td>

<td align="left">number</td>

<td align="left">Год выпуска вашего авто</td>

<td align="left">2016</td>

</tr>

<tr>

<td align="left">* price</td>

<td align="left">object</td>

<td align="left">Цена, за которою вы желаете продать ваше авто</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">value</td>

<td align="left">number</td>

<td align="left">Значение</td>

<td align="left">80000</td>

</tr>

<tr>

<td align="left">currency</td>

<td align="left">object</td>

<td align="left">Валюта в которой вы продаете ваш автомобиль</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">id</td>

<td align="left">number</td>

<td align="left">ID валюты в которой вы продаете ваш автомобиль</td>

<td align="left">1</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">*categories</td>

<td align="left">object</td>

<td align="left">Тип транспорта</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">main</td>

<td align="left">object</td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">id</td>

<td align="left">number</td>

<td align="left">ID типа транспорта</td>

<td align="left">1</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">* brand</td>

<td align="left">object</td>

<td align="left">Марка автомобиля</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">id</td>

<td align="left">number</td>

<td align="left">ID марки автомобиля</td>

<td align="left">5</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">* model</td>

<td align="left">object</td>

<td align="left">Модель автомобиля</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">id</td>

<td align="left">number</td>

<td align="left">ID модели автомобиля</td>

<td align="left">963</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">modification</td>

<td align="left">string</td>

<td align="left">Название модификации вашего автомобиля</td>

<td align="left">V12 AMG B-turbo</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">*body</td>

<td align="left">object</td>

<td align="left">Тип кузова</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">id</td>

<td align="left">number</td>

<td align="left">ID типа кузова</td>

<td align="left">6</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">*mileage</td>

<td align="left">number</td>

<td align="left">Пробег в тыс.км.</td>

<td align="left">32</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">* region</td>

<td align="left">object</td>

<td align="left">Область в которой вы продаете автомобиль</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">id</td>

<td align="left">number</td>

<td align="left">ID области в которой вы продаете автомобиль</td>

<td align="left">10</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">* city</td>

<td align="left">object</td>

<td align="left">Город в котором вы продаете автомобиль</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">id</td>

<td align="left">number</td>

<td align="left">ID города в котором вы продаете автомобиль</td>

<td align="left">10</td>

</tr>

</tbody>

</table>

**Дополнительные параметры**

<table>

<thead>

<tr>

<th align="left">Имя поля</th>

<th align="left">Тип</th>

<th align="left">Описание</th>

<th align="left">Пример</th>

</tr>

</thead>

<tbody>

<tr>

<td align="left">damage</td>

<td align="left">boolean</td>

<td align="left">Ваше авто после ДТП</td>

<td align="left">false</td>

</tr>

<tr>

<td align="left">custom</td>

<td align="left">boolean</td>

<td align="left">Авто растаможено</td>

<td align="left">false</td>

</tr>

<tr>

<td align="left">VIN</td>

<td align="left">string</td>

<td align="left">ВИН код вашего автомобиля</td>

<td align="left">JKBVNCB164A6XXXX</td>

</tr>

<tr>

<td align="left">gearbox</td>

<td align="left">object</td>

<td align="left">Коробка передач</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">id</td>

<td align="left">number</td>

<td align="left">ID коробки передач</td>

<td align="left">1</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">drive</td>

<td align="left">object</td>

<td align="left">Тип привода</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">id</td>

<td align="left">number</td>

<td align="left">ID типа привода</td>

<td align="left">2</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">fuel</td>

<td align="left">object</td>

<td align="left">Тип топлива</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">id</td>

<td align="left">number</td>

<td align="left">ID типа топлива, которое подходит вашему автомобилю</td>

<td align="left">2</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">consumption</td>

<td align="left">object</td>

<td align="left">Расход топлива</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">route</td>

<td align="left">number</td>

<td align="left">Расход топлива по трасе</td>

<td align="left">6</td>

</tr>

<tr>

<td align="left">city</td>

<td align="left">number</td>

<td align="left">Расход топлива по городу</td>

<td align="left">10</td>

</tr>

<tr>

<td align="left">combine</td>

<td align="left">number</td>

<td align="left">Расход топлива в смешеном режиме</td>

<td align="left">8</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">engine</td>

<td align="left">object</td>

<td align="left">Обьем двигателя</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">volume</td>

<td align="left">object</td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">liters</td>

<td align="left">number</td>

<td align="left">Обьем двигателя в литрах</td>

<td align="left">3.5</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">power</td>

<td align="left">object</td>

<td align="left">Мощность вашего авто</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">hp</td>

<td align="left">number</td>

<td align="left">Мощность вашего авто в лошадиных силах</td>

<td align="left">585</td>

</tr>

<tr>

<td align="left">kW</td>

<td align="left">number</td>

<td align="left">Мощность вашего авто в киловатах</td>

<td align="left">430</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">color</td>

<td align="left">object</td>

<td align="left">Цвет</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">id</td>

<td align="left">number</td>

<td align="left">ID цвета вашего автомобиля</td>

<td align="left">10</td>

</tr>

<tr>

<td align="left">metallic</td>

<td align="left">boolean</td>

<td align="left">Цвет металик</td>

<td align="left">true</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">post</td>

<td align="left">object</td>

<td align="left">Добавить торг</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">auctions</td>

<td align="left">boolean</td>

<td align="left">Разрешение добавлять торги к вашему обьявлению</td>

<td align="left">true</td>

</tr>

<tr>

<td align="left">comments</td>

<td align="left">object</td>

<td align="left">Комментарий</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">allowed</td>

<td align="left">boolean</td>

<td align="left">Разрешения комментировать ваше обьявление</td>

<td align="left">true</td>

</tr>

<tr>

<td align="left">check</td>

<td align="left">boolean</td>

<td align="left">Нужно ли ваше подтверждение при добавлении комментария</td>

<td align="left">false</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">exchanges</td>

<td align="left">object</td>

<td align="left">Обмен</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">payment</td>

<td align="left">object</td>

<td align="left">Доплата</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">id</td>

<td align="left">number</td>

<td align="left">Варианты доплаты при добалении обмена к вашему обьявлению</td>

<td align="left">2</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">type</td>

<td align="left">object</td>

<td align="left">Тип обмена</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">id</td>

<td align="left">number</td>

<td align="left">ID типа обмена (на автомобиль,на недвижемость и т.д.)</td>

<td align="left">1</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">video</td>

<td align="left">object</td>

<td align="left">Видео</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">key</td>

<td align="left">string</td>

<td align="left">Ключ к видео на ютубе</td>

<td align="left">lLEiT9PeHSg</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">description</td>

<td align="left">object</td>

<td align="left">Описание</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">ru</td>

<td align="left">string</td>

<td align="left">Описание на русском языке</td>

<td align="left">"Авто в идеальном состоянии, вложений не требует"</td>

</tr>

<tr>

<td align="left">uk</td>

<td align="left">string</td>

<td align="left">Описание на украинском языке</td>

<td align="left">"Авто в ідеальному стані, вкладень не потребує"</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">doors</td>

<td align="left">number</td>

<td align="left">Количество дверей</td>

<td align="left">2</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">seats</td>

<td align="left">number</td>

<td align="left">Количество сидячих мест</td>

<td align="left">2</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">country</td>

<td align="left">object</td>

<td align="left">Странна с которой был пригнан автомобиль</td>

<td align="left"></td>

</tr>

<tr>

<td align="left">import</td>

<td align="left">object</td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">id</td>

<td align="left">number</td>

<td align="left">ID страны</td>

<td align="left">0</td>

</tr>

<tr>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

<td align="left"></td>

</tr>

<tr>

<td align="left">spareParts</td>

<td align="left">boolean</td>

<td align="left">Авто на  запчасти</td>

<td align="left">false</td>

</tr>

</tbody>

</table> 