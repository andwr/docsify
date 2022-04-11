# Docsify

Docsify — это генератор сайтов на базе [NodeJS](https://nodejs.org/en/).

- [x] Поддержка GitHub / GitLab Pages
- [x] Кастомизация CSS, темы
- [x] Отключаемая заглавная страница
- [x] Плагины
- [ ] Не поддерживается рендеринг спецификаций OpenAPI

Документация: https://docsify.js.org/#/?id=docsify

## Примеры документации

* Eleme — [vue-amap](https://elemefe.github.io/vue-amap/#/)
* Alibaba — [weex-ui](https://apache.github.io/incubator-weex-ui/#/)
* Amazon — [style-dictionary](https://amzn.github.io/style-dictionary/#/)
* Microsoft — [Web-Dev-For-Beginners](https://microsoft.github.io/Web-Dev-For-Beginners/#/)

## Ссылки текущего проекта

|  |Repository URL|GitHub Pages URL|
|--|--|--|
|**Origin**|https://github.com/andwr/docsify-fork|https://andwr.github.io/docsify-fork|
|**Upstream**|https://github.com/koshelekapi/docsify|https://koshelekapi.github.io/docsify|

## Ограничения

### Не работает перенос строки в цитате

Хотим получить цитату такого вида:

> Line 1 </br>
> Line 2

Используем разметку:

```markdown
> Line 1
> Line 2

```

Результат:

> Line 1
> Line 2

Чтобы решить эту проблему, можно ввести тег переноса строки:

```markdown
> Line 1 </br> 
> Line 2

```

Результат:

> Line 1 </br>
> Line 2