### Общие Ошибки Веб-Службы

Определенные распространенные ошибки будут возвращены стандартным способом из всех веб-сервисов API RIA.com. Кроме того, некоторые сообщение об ошибках могут быть специфичными для некоторых сервисов (см. документацию для конкретного сервиса). Ниже описаны распространенные ошибки:

<table>
<thead>
                <tr>
                    <th class="doc-parameters-name" scope="col" style="width: 100px;">Error Code</th>
                    <th class="doc-parameters-name" scope="col" style="width: 100px;">HTTP Status Code</th>
                    <th class="doc-parameters-required" scope="col">Описание</th>
                </tr>
                </thead>
                <tbody>
                <tr>
                    <th class="doc-parameter-name" scope="row">API_KEY_MISSING</th>
                    <td class="doc-parameter-name">403</td>
                    <td class="doc-parameter-description">
                        API ключ не был указан. Подробнее об
                        <a href="/docs/api-key/">использовании</a> API ключа см. в разделе “Использование API Key” .
                    </td>
                </tr>
                <tr>
                    <th class="doc-parameter-name" scope="row">API_KEY_INVALID</th>
                    <td class="doc-parameter-name">403</td>
                    <td class="doc-parameter-description">
                        Был указан неверный ключ API. Убедитесь, что был указан корректный API ключ, или
                        <a href="/signup/">зарегистрируйтесь</a> для получения ключа.
                    </td>
                </tr>
                <tr>
                    <th class="doc-parameter-name" scope="row">API_KEY_DISABLED</th>
                    <td class="doc-parameter-name">403</td>
                    <td class="doc-parameter-description">
                        API ключ был отключен администратором. Пожалуйста
                        <a href="/contact/">свяжитесь с нами</a> для помощи.
                    </td>
                </tr>
                <tr>
                    <th class="doc-parameter-name" scope="row">API_KEY_UNAUTHORIZED</th>
                    <td class="doc-parameter-name">403</td>
                    <td class="doc-parameter-description">
                        API ключ не авторизован для доступа к данному сервису. Пожалуйста
                        <a href="/contact/">свяжитесь с нами</a> для помощи.
                    </td>
                </tr>
                <tr>
                    <th class="doc-parameter-name" scope="row">API_KEY_UNVERIFIED</th>
                    <td class="doc-parameter-name">403</td>
                    <td class="doc-parameter-description">
                        API ключ не подтвержден. Проверьте свою электронную почту для подтверждения API ключа. Пожалуйста
                        <a href="/contact/">свяжитесь с нами</a> для помощи.
                    </td>
                </tr>
                <tr>
                    <th class="doc-parameter-name" scope="row">HTTPS_REQUIRED</th>
                    <td class="doc-parameter-name">400</td>
                    <td class="doc-parameter-description">Запросы к этому API должны быть произведены по HTTPS протоколу.                                                            Убедитесь, пожалуйста, что Вы используете HTTPS протокол для Вашего                                                          запроса.
                    </td>
                </tr>
                <tr>
                    <th class="doc-parameter-name" scope="row">OVER_RATE_LIMIT</th>
                    <td class="doc-parameter-name">429</td>
                    <td class="doc-parameter-description">
                        Превышен лимит запросов для данного API ключа.
                        <a href="/contact/">Свяжитесь с нами</a> для получения дополнительной информации о
                        <a href="/docs/rate-limits/"> лимитах веб-сервисов</a> .
                    </td>
                </tr>
                <tr>
                    <th class="doc-parameter-name" scope="row">NOT_FOUND</th>
                    <td class="doc-parameter-name">404</td>
                    <td class="doc-parameter-description">
                        Не удалось найти API по данному URL-адресу. Проверьте свой URL.
                    </td>
                </tr>
                </tbody>
            </table>
