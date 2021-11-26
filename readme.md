# Стартовый проект для вёрстки
---
Обязательно добавьте поддержку [editorconfig](https://editorconfig.org/#download) в ваш редактор кода.

```bash
npm i             # установить зависимости
npm start         # запустить сервер разработки (остановить: Ctrl+C)
npm build         # запустить сборку проекта
npm run bemlint   # проверить html-файлы папки build на соответствие BEM
npm run puglint   # проверить pug-файлы
npm run stylelint # проверить scss-файлы
```

Перед коммитом происходит автопроверка файлов. Если проверка выявила ошибки, они будут показаны в терминале.

---
## О сборке:
### в составе:
- Sass (SCSS)
- PostCSS
  - Autoprefixer
  - PostCSS Flexbugs Fixes
    https://github.com/luisrudge/postcss-flexbugs-fixes
  - PostCSS animation
    https://github.com/zhouwenbin/postcss-animation
- Pug (Jade)
- stylelint
- eslint
- puglint
- Babel
- GitPages
- gulp.spritesmith

### файл config.js

Файл **`config.js`** содержит глобальные настройки проекта в объекте `config`:

> **dir** — переменные директорий проекта
> **addAssets** — дополнительные файлы проекта
> **options** — флаги, если нужно отключить какую-то часть сборки (например, в случае полной ненадобности js или сторонних модулей (Vendors)):
>* **copyAssets** — включает/выключает копирование дополнительных файлов проекта
>* **processJs** — включает/выключает создание `/js/script.min.js` и отслеживание изменений в js-файлах
>* **copyJsVendors** — включает/выключает обработку дополнительных js-модулей и создание `/js/vendors.min.js`
> при **`processJs`**` = false` и **`processJs`**` = false` папка `/js` не создается
>* **typescript** — включает/выключает компиляцию ts-файлов и удаляет папку `/ts` при **`typescript`**` = false`

### gh-pages
Модуль `gh-pages` для публикации результатов верстки уже установлен

```bash
npx gulp deploy  # инициализация
npm start deploy # отправка последнего коммита
```
---

## Справочная информация

- [Как работать с CSS-препроцессорами и БЭМ](http://nicothin.github.io/idiomatic-pre-CSS/)
- [Шпаргалка по bash](https://github.com/nicothin/web-development/tree/master/bash)
- [Шпаргалка по консольным командам Git](https://github.com/nicothin/web-development/tree/master/git)
- [Шпаргалка ниндзя Sublime Text 3](http://nicothin.github.io/sublime-text/sublime-text-3-hotkeys.html)
- [Sublime Text 3 для работы с фронтэндом](https://github.com/nicothin/sublime-text)
- [Шпаргалка по подключению gh-pages к проекту](https://nicothin.pro/page/gh-pages)
