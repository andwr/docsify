# OpenAPI

!> **Внимание.** Обработка спецификаций OpenAPI в формате YAML, JSON не поддерживается.

## express-jsdoc-swagger

> Источник: https://brikev.github.io/express-jsdoc-swagger-docs/#/

Этот плагин предполагает использование файлов JavaScript для оформления спецификаций OAS (код спецификации оформляется в виде комментария к JS-скрипту). Чтобы этот вариант заработал, помимо NodeJS необходимо дополнительно установить пакет `express-jsdoc-swagger`:

```bash
npm i express-jsdoc-swagger
```

Проверку работы этого способа я не выполнял.

### Пример

Исходный код в файле JavaScript:

```javascript
/**
 * POST /api/v1/song
 * @param {Song} request.body.required - Song info
 * @return {object} 200 - Success response
 * @return {object} 400 - Bad request response
 * @example request - example payload
 * {
 *   "title": "Bury The Light",
 *   "artist": "Casey Edwards ft. Victor Borba",
 *   "year": 2020
 * }
 * @example request - other payload example
 * {
 *   "title": "The war we made",
 *   "artist": "Red",
 *   "year": 2020
 * }
 * @example response - 200 - example success response
 * {
 *   "message": "You have added a song!"
 * }
 * @example response - 400 - example error response
 * {
 *   "message": "Failed to save song because you did not specify a title",
 *   "errCode": "EV121"
 * }
 */
app.post('/api/v1/song', (req, res) => res.send({
  message: 'You have added a song!',
}));
```

Результат:

![image](https://brikev.github.io/express-jsdoc-swagger-docs/assets/examples.png)

