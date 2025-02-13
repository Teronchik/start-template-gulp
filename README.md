# Project-start-template (Gulp)
Стартовий шаблон для проекту на основі таск-менеджера Gulp
___
## Команди для використання
`npm install` – встановлення пакетів та залежностей<br><br>
`npm test` – запуск перевірки наявності стилістичних помилок<br><br>
`npm start` – збирання проекту в режимі розробки із запуском локального сервера<br><br>
`npm run build` – фінальне збирання проекту <br><br>
`npm run deploy` – фінальне збирання проекту із деплоєм його в [GitHub Pages](https://pages.github.com)<br><br>
`npm run dist` – фінальне збирання проекту із архівацією його в форматі zip<br>
___
## Як використовувати проект
Налаштування плагінів винесено у файл `gulpfile.babel.js/config/app.js`.  Шляхи до файлів, що обробляються задачами винесено у файл `gulpfile.babel.js/config/paths.js`.<br>
Усі задачі знаходяться в каталозі `gulpfile.babel.js/tasks/`. Наявна можливість створення і підключення інших задач або видалення існуючих при необхідності. Для підключення власної задачі додайте її у вище вказаний каталог та  імпортуйте її у файл `gulpfile.babel.js/index.js`.
___
## Опис задач і плагінів
* `gulp-load-plugins` – спрощення процесу підключення Gulp плагінів
* `gulp-plumber` – відстежування помилки, які можуть виникнути при виконанні задач
* `gulp-notify` – вивід сповіщення, наприклад, у разі помилки
* `gulp-size` – показ розмірів файлів
* `gulp-rename` – перейменовування файлів
* `gulp-newer` – відстеження тільки тих файлів, які було змінено
* `gulp-if` – можливість використання умовних конструкцій в задачах
* `gulp-zip` – створення та редагування `zip` архівів
* `del` – видалення каталогів і файлів
### HTML
Використовується за замовчуванням
* `gulp-file-include` – надання можливостей для шаблонізації `html` файлів
* `gulp-webp-html` – додавання в розмітку `webp` зображення
* `gulp-htmlmin` – мініфікація `html` файлів
* `gulp-html-bem-validator` – перевірка БЕМ синтаксису
### Pug
Використовується замість задачі HTML при користуванні шаблонізатором Pug
* `gulp-pug` – конвертація `pug` файлів у `html`
### CSS
* `gulp-concat` – об'єднуання всх `css` файлів в один
* `gulp-cssimport` – вставка вмісту `css` файлу замість `@import`
* `gulp-autoprefixer` – додавання вендорних префіксів
* `gulp-group-css-media-queries` – групування медіа запитів
* `gulp-csso` – мініфікація `css` файлів
* `gulp-shorthand` – заміна розгонутий опис стилів скороченим
### Sass
Використовується замість задачі CSS при користуванні препроцесором SASS
* `gulp-sass-glob` – імпорт в `sass` цілих каталогів / імпорт за шаблонами
* `sass`,`gulp-sass` – конвертація `sсss` файлів у `сss`
### Fonts
* `gulp-fonter` – конвертація різних шрифтових форматів
* `gulp-ttf2woff2` – конвертація шрифтів `ttf` у формат `woff2`
### Images
* `gulp-webp` – конвертація растрових зображень в формат `webp`
* `gulp-imagemin` – оптимізація та мініфікація зображень
### Scripts
* `gulp-babel` – переписування коду на ES6 (ES-2015) в код на попередніх стандартах
* `webpack` – пакувальник модулів для JavaScript
### Server
* `browser-sync` – створення і запуск локального сервера
### Clear
Видалення каталогу `build`
### Copy
Копіювання каталогу `favicon` у готовий проект
### Zip
Створення каталогу `dist` із `zip` архівом, у якому знаходиться зібраний проект
