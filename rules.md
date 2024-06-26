# Язык разметки Markdown
Базовым Markdown уже мало кто пользуется. Зато у него существуют спецификации и диалекты, которые добавляют в язык новые функции: встраивание HTML-тегов, создание таблиц и чекбоксов, зачёркивание текста, разные варианты переноса строки.
## Параграфы и разрывы строк
Чтобы поделить текст на параграфы, между ними нужно оставить пустую строку. Строка считается пустой, даже если в ней есть пробелы и табуляции. Если же строки находятся рядом, то они автоматически склеиваются в одну.

Так (пробел)

Вот так

Для переноса строки внутри одного параграфа есть три метода:

* поставить в конце строки два или больше пробела   ;
* поставить в конце строки обратную косую черту \;
* использовать HTML-тег "< br >".

## Заголовки 
В синтаксисе Markdown есть шесть уровней заголовков: от H1 (самого большого) до H6 (самого маленького). Для их выделения используют решётки #, при этом есть несколько тонкостей:

решётки можно ставить как перед заголовком, так и с двух сторон от него (на уровень заголовка влияют только те #, которые находятся перед ним);
количество решёток соответствует уровню заголовка: одна для первого уровня, две для второго и так далее;
между решёткой и текстом ставится пробел. 

У заголовков первого и второго уровня есть альтернативный способ выделения: на следующей строке после них нужно поставить знаки равенства = или дефисы -. Вот несколько правил:

знак = применяется для заголовков H1;
дефис применяется для заголовков H2;
если в одной строке поставить оба знака, то работать ничего не будет;
можно ставить любое количество знаков, и на тип заголовка это не повлияет;
между заголовком и знаками не должно быть пустых строк.
## Выделение текста 
Чтобы изменить начертание текста, нужно выделить его с двух сторон спецсимволами следующим образом: <спецсимвол>текст<спецсимвол>.
## Жирный 
Для выделения текста жирным нужно использовать две звёздочки ** или два нижних подчёркивания __.

**Жирный**

## Жирный курсив 
Для выделения текста сразу обоими стилями нужно использовать три звёздочки *** или три нижних подчёркивания ___.

***Жирный курсив***
## Зачёркнутый
Чтобы зачеркнуть текст, нужно использовать две тильды ~~. Такая опция есть только в диалекте GitHub Flavored Markdown.

~~Зачёркнутый~~
## Подчёркнутый (underline)
В синтаксисе Markdown нет встроенного способа подчеркнуть текст. Но если ваш редактор поддерживает HTML, то можно использовать теги < u > и < /u >:

<u>Подчёркнутый</u>
## Ссылки (links)
Самый лёгкий способ поместить ссылку в Markdown — заключить её в угловые скобки. Несмотря на простоту, он не является основным и был добавлен только в спецификации CommonMark.

<https://gb.ru/>
## Таблицы 
В уже упомянутом выше диалекте GitHub Flavored Markdown (и некоторых других тоже) есть возможность оформлять таблицы. Столбцы разделяются вертикальными линиями |, а строка с шапкой отделяется от остальных дефисами -, которых можно ставить сколько угодно.

|1 столбец|2 стоблец| 3 стобец|
|----|--|---|
|АДЫН|ДВА|ТРЫ|

## Нумерованные списки 
Для создания нумерованного списка перед пунктами нужно поставить число с точкой. При этом нумерация в разметке ленивая. Неважно, какие именно числа вы напишете: Markdown пронумерует список автоматически.

1. а
2. б
3. с 

## Ненумерованные списки 
Для создания ненумерованного списка нужно поставить перед каждым пунктом звёздочку *, дефис - или плюс +.

* а 
* б
* с

Обратите внимание, что Markdown относит к разным спискам пункты, перед которыми стоят разные маркеры. Даже несмотря на то, что мы не оставляем пустых строк между списками.

Если же два списка идут подряд, а перед их пунктами стоят одинаковые маркеры, тогда между ними нужно отбить две пустые строки (как в случае с нумерованными списками).