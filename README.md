# goit-markup-hw-08

Проект

«A1» Используется методология BEM.

«A2» Ипользуется препроцессов SASS.

«A3» В файлах index.html и portfolio.html подключен минифицированный файл стилей
main.min.css из папки css.

«A4» При просмотре страницы на любом устройстве шириной от 320px, не появляется
горизонтальная полоса прокрутки.

«A5» Скрипт мобильного меню подключен в HTML отдельным файлом mobile-menu.js.

Разметка «B1» У всех страниц в блоке <head> есть метатег viewport.

«B2» Все фоновые и контентные растровые изображения - отзывчивые, и поддерживают
экраны с плотностью x1 и x2.

«B3» Для отзывчивых контентных изображений использован элемент <img> с атрибутом
srcset и дескриптором x.

«B4» Для отзывчивых фоновых изображений использованы медиа-фукцнии
min-device-pixel-ratio и min-resolution.

«B5» Выполнена разметка мобильного меню.

Оформление «C1» При написании стилей использован Mobile First подход и
медиа-функция (min-width: ).

«C2» Стили необходимые только в определённом промежутке, закрыты в медиа-запросы
(min-width: ) and (max-width: ) или только (max-width: ).

«C3» В медиа-запросах отсутствует лишнее дублирование стилей.

«C4» Вёрстка выполнена относительно трёх точек перелома: 480px, 768px и 1200px.

«C5» Выполнено оформление мобильного меню.

================= start js ====================== Открытие мобильного меню

Мобильное меню открывается по клику на кнопку "бургера". Для того чтобы скрипт
сработал необходимо добавить в разметку специальные атрибуты, по которым скрипт
ищет элементы:

data-menu-button - на кнопку открытия мобильного меню(бургер) data-menu-close -
на кнопку закрытия мобильного меню(крестик) data-menu - на мобильное меню После
чего, перед закрывающим тегом body добавить тег script со ссылкой на файл
скрипта для мобильного меню.

<body>
  <!-- Ставим перед закрывающим тегом body -->
  <script src="./js/mobile-menu.js"></script>
</body>
Вот скрипт который необходимо скопировать и вставить в файл скрипта mobile-menu.js.

(() => { const menuBtnRef = document.querySelector("[data-menu-button]"); const
mobileMenuRef = document.querySelector("[data-menu]"); const mobileBtnClose =
document.querySelector("[data-menu-close]");

menuBtnRef.addEventListener("click", () => {
mobileMenuRef.classList.toggle("is-open"); });

mobileBtnClose.addEventListener("click", () => {
mobileMenuRef.classList.toggle("is-open"); }); })();

Изначально мобильное меню должно быть скрыто, например с помощью:

.mobile-menu { opacity: 0; visibility: hidden; pointer-events: none; } Мобильное
меню открывается когда на него вешается клас is-open. Нужно описать еще этот
клас, например:

.mobile-menu.is-open { opacity: 1; visibility: visible; pointer-events: auto; }
================= end js ======================

правила для девайсов которые работают так как указанно в макете

// mobile мобилный @media screen and (max-width: 480px) { .section { max-width:
480px; } }

// tablet планшет @media screen and (min-width: 768px) { .section { min-width:
768px; } }

// desktop пк @media screen and (min-width: 1200px) { .section { min-width:
1200px; } }
