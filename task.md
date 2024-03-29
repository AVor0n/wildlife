# wildlife

Задание: сверстать страницу согласно макету.

![wildlife](https://github.com/rolling-scopes-school/stage0/raw/c57cba156d3b692821a1c9902eaf13379c8d68ee/stage0/tasks/images/wildlife.jpg)

**[Макет Wildlife](https://www.figma.com/file/dJoqHi1YHTLR06PPEeCc7t/Wildlife)**

- Точное совпадение с макетом не требуется. Основное требование - визуальное сходство вёрстки и страницы макета. Допускается отклонение от макета на 5px по горизонтали и 10px по вертикали.
- Адаптивность не проверяется, но рекомендуется. Постарайтесь сделать сайт адаптивным, то есть подстраивающимся под размер экрана и отображающимся на небольших экранах без появления полосы прокрутки.
- Работающий слайдер не требуется, но если можете - сделайте.
- Если в строке несколько объектов визуально одинаковой ширины, то ширина содержащих их блоков должны быть одинаковой.
- «Интерактивный» означает, что у элемента появляется визуальный эффект или анимация при каких-либо действиях пользователя, например, при наведении курсора или нажатии. Обычно такой эффект реализуют при помощи следующих свойств:
  - `cursor: pointer`,
  - `background`,
  - `text-decoration: underline`,
  - `color`
- Ширина макета 1440px, ширина контентной части 1200px. Макет позиционируем по центру с равными отступами по краям. Блокам задаём цвет фона, растягивая их во всю ширину экрана. Блоки Header и Survival - `background-color: #02160b`, блоки Latest articles и Get notified `background-color: #cccccc`, блок Footer - `background-color: #181617`.
- Фоновые изображения могут как оставаться в пределах 1440px, так и растягиваться во всю ширину страницы.
- требования к вёрстке отдельных блоков указаны в критериях оценки.

## Требования к коммитам

- История коммитов должна отображать процесс разработки приложения.
- [Названия коммитов дайте согласно гайдлайну](https://docs.rs.school/#/git-convention)

## Технические требования

- Вёрстка проверяется в браузере Google Chrome последней версии
- Запрещается использование CSS-фреймворков (bootstrap, foundation и т.д.)
- Допускается использование CSS препроцессоров, normalize.css

## Критерии оценки

**Максимальный балл за задание +50**

#### 1. Блок **Header** +10

- Блок Header содержит только логотип и панель навигации. Наличие блоков-обёрток во внимание не принимаем
- Логотип содержит два элемента - svg-иконку и текст. SVG может быть добавлен любым способом. Обращаем внимание на формат, а не на способ добавления
- На странице обязательно должен присутствовать один элемент `<h1>`. Расположите его на свое усмотрение. Не проверяем какой именно элемент указан как h1, главное, чтобы он был и был только один
- Панель навигации состоит из четырёх элементов: двух ссылок, иконки поиска и кнопки "Sign in" . Верстается в виде ненумерованного списка: `ul > li > a`. Если кнопка "Sign in" верстается не как ссылка, а тегом button, это не ошибка
- Все элементы панели навигации должны быть интерактивными

#### 2. Блок **Survival** +10

- Расстояние между буквами заголовка регулируется css-свойством `letter-spacing`
- Разрывы строк в текстовом блоке регулируются шириной блока без использования тега `<br>`
- Кнопка Donate интерактивная. Используются указанные в макете стили для различных состояний кнопки
- У блоков Header и Survival общее фоновое изображение

#### 3. Блок **Latest articles** +10

- Для вёрстки трёх изображений в ряд лучше использовать [flexbox](https://habr.com/ru/post/467049/) или [grid](https://tuhub.ru/posts/css-grid-complete-guide). Float использовать можно. `<table>` - нельзя!
- Надписи поверх изображений можно разместить при помощи абсолютного позиционирования. Менее семантически правильный, но более простой в реализации вариант - использовать для добавления изображений css-свойство `background-image`.
- Стрелки слайдера интерактивны.

#### 4. Блок **Get notified** +10

- Для отправки данных используется тег `<form>`
- Поле email верстается тегом `<input>` с типом `text` или `email` (оба варианта допустимы), поле send верстается тегом `<input>` с типом `submit`
- Надпись 'email' это placeholder.

#### 5. Блок **Footer** +10

- Блок Footer содержит логотип, дополнительную панель навигации и ссылки на социальные сети
- Логотип полностью повторяет логотип блока Header. Речь о визуальном сходстве, а не использовании точно таких же тегов
- Дополнительная панель навигации и ссылки на социальные сети верстаются в виде ненумерованных списков: `ul > li > a`
- Иконки социальных сетей верстаются с использованием svg-файлов в качестве фоновых изображений
- Все ссылки в футере должны быть интерактивными

## Pixel Perfect. Штрафные баллы

- В первую очередь обращаем внимание на визуальное сходство созданного сайта и макета.
- Проверку Pixel Perfect стоит проводить в разрешении экрана десктопа (окна операционный системы на мониторе) 100%.
- Если разрешение вашего экрана меньше ширины макета (1440px), проверка проводится с применением device toolbar при помощи выставления там ширины 1440 в режиме responsive
- В браузере Google Chrome при помощи расширения [PerfectPixel](https://chrome.google.com/webstore/detail/perfectpixel-by-welldonec/dkaagdgjmgdmbnecmcefdhjekcoceebi) проверяем соответствие наложения импортированного из figma изображения макета на страницу сайта.
- Если визуальные отличия элементов или блоков составляют более 5px по горизонтали или более 10px по вертикали, то ставим **-2** балла единовременно за каждый логический блок, в котором присутствует ошибка. Сами блоки при этом рассматриваются по раздельности, т.е. недочеты предыдущего блока не переносятся на следующий, а при переходе проверки на следующий блок, мы его выравниваем с наложенным изображением.
- Относительно текста проверяем размеры только по высоте. Ширину слов и отступ между буквами не учитываем при сопоставлении макета и вёрстки.
- Общее количество баллов за блок с учётом штрафных баллов не может быть ниже нуля.
- Не является ошибкой замена в footer приложения иконки Telegram на иконку YouTube
- Проверяем только положение элементов на странице, на возможные отличия в положении фонового изображения внимания не обращаем, баллы за это не снимаем
