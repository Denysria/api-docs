### Статистика объявления

Чтобы получить статистику об обьявлении, Вам необходимо выполнить GET запрос такого вида:

https://developers.ria.com/auto/used/autos/advertisementId/statistic?user_id=Ваш ID&api_key=YOUR_API_KEY

или `curl -X GET "https://developers.ria.com/auto/used/autos/advertisementId/statistic?user_id=Ваш ID&api_key=YOUR_API_KEY" -H "accept: application/json"`

, где *user_id* - Ваш ID в системе RIA.com, *advertisementId* - ID нужного Вам объявления, *api_key* - Ваш ключ.

**Пример запроса**

`curl -X GET "https://developers.ria.com/auto/used/autos/20268839/statistic?user_id=7069830&api_key=YOUR_API_KEY" -H "accept: application/json""`

**Пример успешного ответа:**

```json
{
  "views": 329,
  "clicks": 24
}
```
Расшифровка параметров:

- *views* - Количество просмотров объявления
- *clicks* - Количество открытий номера телефона

 Полное описание сервиса "Статистика объявления" описаный с помощью стандарта **DeFacto swagger 2.0** [здесь](http://swagger.ria.com/ui/?api=auto/advertisements#/)
