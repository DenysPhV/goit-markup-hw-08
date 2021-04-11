# goit-markup-hw-08

Разметка

«B5» Выполнена разметка мобильного меню.

Оформление

«C2» Стили необходимые только в определённом промежутке, закрыты в медиа-запросы
(min-width: ) and (max-width: ) или только (max-width: ).

«C3» В медиа-запросах отсутствует лишнее дублирование стилей.

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

// mobile мобилный @media screen and (min-width: 480px) { .section { max-width:
480px; } }

// tablet планшет @media screen and (min-width: 768px) { .section { min-width:
768px; } }

// desktop пк @media screen and (min-width: 1200px) { .section { min-width:
1200px; } }
