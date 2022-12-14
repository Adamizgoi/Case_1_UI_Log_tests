# Проект в разработке...

# Case_1_UI_Log_tests
Кейс по ручному тестированию верстки и логов **без документации**. 

Задание: 
"Вам предлагается протестировать сайт https://www.saucedemo.com/.
В этом кейсе оценивается ваша логика мышления, аналитические навыки. 

Необходимо создать чек-лист для проверки верстки и логи работы интернет-магазина. Обратите внимание, что для логина предусмотрены 4 типа пользователей. Если будут найдены какие-то баги, просьба оформить их на отдельном листе в том же документе".

## Дата старта
22:30
9.09.2022
4 часа 

20:40
14.09.2022
5 часов 

## Дата финиша

## Тестирование верстки
Тестирую только "тестовый стенд с последним билдом". Сайт https://www.saucedemo.com/ c логином standard_user и паролем secret_sauce
Остальные билды содержат множество функциональных багов, которые поправлены в билде standard_user

### Вспомогательные материалы
**Прикладные (моего авторства)**

Таблица переходов и состояний https://drive.google.com/file/d/1MzBZW0oX_njttbFoHGZROr533mWDU2kR/view?usp=sharing

**Теоритические**

1. Чек-лист тестирования верстки [https://habr.com/ru/post/114256/](https://habr.com/ru/post/114256/) (староват, но всеобъемлющий)

2. Тестирование адаптивной верстки [https://win-keys.ru/windows-8/testirovanie-adaptivnogo-dizaina-luchshie-instrumenty-dlya-testirovaniya.html](https://win-keys.ru/windows-8/testirovanie-adaptivnogo-dizaina-luchshie-instrumenty-dlya-testirovaniya.html)

3. Попарное тестирование на кейсе тестирования UI [https://www.saucedemo.com/inventory.html](https://www.saucedemo.com/inventory.html)

4. State & Transition Diagram — что это и как применять [https://habr.com/ru/post/548192/](https://habr.com/ru/post/548192/)

5. Рейтинг популярности браузеров в мире десктоп и мобайл (апрель, 2022) [https://www.seonews.ru/events/samye-populyarnye-brauzery-v-mire-v-aprele-2022-goda-reyting/](https://www.seonews.ru/events/samye-populyarnye-brauzery-v-mire-v-aprele-2022-goda-reyting/)

6. Рейтинг распространенности размеров экранов ПК (2022) [https://ru.screenresolution.org/year-2022/](https://ru.screenresolution.org/year-2022/)

7. Обзор WCAG 3.0 [https://web-standards.ru/articles/wcag3-changes/](https://web-standards.ru/articles/wcag3-changes/)

8. Тестирование верстки [https://quality-lab.ru/blog/layout-testing/](https://quality-lab.ru/blog/layout-testing/)

### План проверки
Подготовка к тестированию
1. Сделать таблицу переходов и состояний для десктоп и мобильной версии сайтов 
2. Сделать таблицу pairwise testing для кроссбраузерного тестирования (браузеры, версии) и тестирования разных гаджетов (мобайл и ПК)

#### Мой чек-лист
##### Тестирование внешнего вида
1. Исследовательское состояние дизайна сайта по таблице переходов и состояний
2. Тестирование браузеров / гаджетов / размеров экрана:
- разные браузеры (хром, яндекс, сафари, мазила, эдж, опера, самсунг интернет, explorer - почастоте использования (и приоритетности тестирования), согласно статистике)
- мобайл (разные марки и модели смартфонов с разными размерами экрана)
- десктоп (разные марки и модели компьютеров и ноутбуков с разными размерами экрана (в web tools есть переключатель размеров)
- планшеты (разные марки и модели)
3. Адаптивная верстка. Состояние сайта при использовании инструмента "изменение масштаба" в браузере
4. Дизайн сайта при неполадках в интернете: JS / файлы не загружаются
5. Использованы ли в CSS "запасные" семейства шрифтов, которые поддерживаются всеми браузерами и гаджетами
6. Тестирование по стандарту доступности WCAG 3.0
7. Если останется время. В разных комбинациях браузер + гаджет + размер экрана из популярных + масштабирование + состояние из таблицы №1 (тут, теоритически, поможет попарное тестирование)
8. Все ли ок со ссылками
9. Реагируют ли кликабельные элементы на наведение на них мышью

##### Тестирование юзабилити

P.S. в процессе тестирования буду ориентироваться на чек-лист из приложенных теоретических материалов, в нем есть пункты, которые я не учла

#### Инструменты
1. Валидатор JavaScript
https://tools.icoder.uz/javascript-validator.php
2. Валидатор HTML
[https://validator.w3.org/nu/?doc=https%3A%2F%2Fwww.saucedemo.com%2F](https://validator.w3.org/nu/?doc=https%3A%2F%2Fwww.saucedemo.com%2F)
3. Валидатор CSS
4. Майнд-карты https://www.mindmeister.com/folders
5. Расширение для браузера PageRuler
6. Эмулятор разных устройств Lambda https://app.lambdatest.com/
7. ПО для Windows - эмулятор Mac VirtualBox (Mac OS Sierra 10.12)

P.S. так как нет макета и другой документации, я не использую браузерные расширения для измерения, например, расстояния между элементами, или для вычисления цвета элементов. 

#### Ход тестирования
Проверяю по чек-листу из приложенных материалов, он более полный. Из своего чек-листа добавлю в конце проверки pairwise testing 

1. Проверяю кодировку сайта через Web tools в коде HTML. UTF-8.**ОК**
2. Там же. Проверяю DOCTYPE - HTML. **ОК** 
3. Составляю таблицу переходов и состояний перед.
4. Анализирую дизайн сайтов согласно таблице переходов и состояний + фиксирую баги
5. Изучаю состояние сайта при изменении размера окна браузера (в самом популярном браузере Chrome) + фиксирую баги 
6. Провожу кросс-браузерное тестирование для приоритетных ПК браузеров (теоритические материалы, пункт 5) в ПК (Edge, Firefox последний, Safari на эмуляторе, Firefox, Opera, Explorer) + фиксирую баги
7. Провожу кросс-браузерное браузерное тестирование для приоритетных браузеров (теоритические материалы, пункт 5) для мобильных устройств (Chrome, Safari)
8. Проверяю валидаторами код CSS всех страниц и HTML код только вводной страницы (тут защита html от копирования, копировать сайт только вручную остается, в реальных условиях запросила бы код). В web-tools/источники CSS вручную копирую все файлы CSS всех страниц в валидатор - **ОК**
9. Проверить микроданные на чужом проекте не представляется возможным 
10. Как сайт выглядит с выключенными картинками
