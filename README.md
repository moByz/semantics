# Семантика html
## https://habr.com/ru/post/240065/
## Что такое семантическая верстка
Семантическая вёрстка веб-страницы или семантический код HTML-документа – это вёрстка с правильным использования HTML-тегов в соответствии с их предназначением (семантикой). Кроме этого, семантическая вёрстка предполагает логичную и последовательную иерархию для построения всей веб-страницы, в соответствии с законами HTML-документа.
### Чем отличается семантическая вёрстка от обычной
Семантическая вёрстка веб-документа противопоставляется обычной, при котором написание HTML-кода определяется только внешним видом веб-страницы. При семантической вёрстке, ряд элементов страницы имеют свои собственные теги, которые прямо отображают их назначение.
### Почему стоит использовать семантику
Семантические элементы четко описывают, что они означают как веб-разработчику так и браузеру. В HTML4 веб-разработчики использовали свои собственные имена в идентификаторах/классах элементов для их стилизации: header, top, bottom, footer, menu, navigation, main, container, content, article, sidebar, topnav и т.п. Такое положение дел не позволяло поисковым системам корректно идентифицировать роль того или иного контента веб-страницы. Благодаря новым элементам HTML5, сделать это стало гораздо проще.
## Основные семантические теги html5
### header 
Группирует вводные и навигационные элементы, не является обязательным. Может содержать заголовки, оборачивать содержание раздела страницы, форму поиска или логотип. В HTML-документе может содержаться одновременно несколько элементов header и они могут располагаться в любой части страницы. Элемент header нельзя помещать внутрь элементов footer, address или другого элемента header.
### article
Используется для группировки записей — публикаций, статей, записей блога, комментариев. Представляет собой независимый обособленный блок, предназначенный для многократного использования, как правило, начинается с заголовка.
### nav 
Предназначен для создания блока навигации веб-страницы или всего веб-сайта, при этом не обязательно должен находиться внутри header. На странице может быть несколько элементов nav.
### aside 
Группирует содержимое, связанное с окружающим его контентом напрямую, но которое можно счесть отдельным (т.е., удаление этого блока не повлияет на понимание основного содержимого). Чаще всего элемент позиционируется как боковая колонка (как в книгах) и включает в себя группу элементов: nav, цифровые данные, цитаты, рекламные блоки, архивные записи. Не подходит для блоков, просто позиционированных в стороне.
### main
Элемент main представляет основное содержимое документа (содержимое элемента body). Контент, находящийся внутри элемента, должен быть уникальным и не повторяться во всех документах сайта, таких как навигационные ссылки, информация о копирайте, логотипы, формы поиска (в случае, если форма поиска является основной функцией документа).
### section 
Элемент представляет собой универсальный раздел документа. Группирует тематическое содержимое и обычно содержит заголовок.
### footer
Представляет собой нижний колонтитул содержащей его секции или корневого элемента. Обычно содержит информацию об авторе статьи, данные о копирайте и т.д. Если используется как колонтитул всей страницы, содержимое дополняется сведениями об авторских правах, ссылками на условия использования, контактную информацию, ссылками на связанное содержимое и т.п.

В одном веб-документе может быть несколько элементов footer.
### address
Используется для определения контактной информации автора/владельца документа или статьи. Для обозначения автора документа тег размещают внутри элемента body, для отображения автора статьи — внутри тега article.
## Атрибуты
### role
Атрибут role, позволяет наиболее четко указать назначение блока/элемента страницы при взаимодействии пользователя с сайтом.
#### Основные и наиболее часто используемые значения role:
```
1. banner - содержит главный заголовок или внутренний заголовок страницы. Например логотип и название сайта. Рекомендуется использовать не больше одного раза на странице.
2. complementary - информационный блок, отделенный от основного содержания ресурса.
3. contentinfo - обобщающая информация о содержании страницы (к примеру футер сайта). Рекомендуется использовать не больше одного раза на странице.
4. definition - указывает определение термина или понятия.
5. main - выступает в качестве основного содержания документа. Рекомендуется использовать не больше одного раза на странице.
6. navigation - набор элементов предназначенных для навигации по документу или связанным документам. Рекомендуется использовать не больше одного раза на странице.
7. note - заметка (вспомогательная информация) к основному содержанию ресурса.
8. search - указывает область для поиска по содержимому.
```
### aria-label
Атрибут aria-label позволяет задать дополнительную текстовую метку, которая будет пояснять назначение данного блока. Причём важно понимать, что aria-label именно дополняет role, поэтому не надо в её тексте дублировать информацию о семантическом назначении блока, например, совсем не нужно для nav писать, что это «Область навигации по разделам», достаточно просто написать «Разделы».
