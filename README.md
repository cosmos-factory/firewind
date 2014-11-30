FireWind
========

Поисковый движок, использующий морфологический анализатор phpMorphy. Возможности:

* **Поиск с учетом языковой морфологии.** Не зависимо от падежа, окончания и 
	других прелестей великого и могучего языка поиск должен находить то, что нужно 
	пользователю. Другими словами, "яблок", "яблока", "яблоки" - это формы одного и того 
	же слова "яблоко", что нужно учитывать в поисковом алгоритме. Одним из способов 
	достижения данной цели является приведение каждого слова поискового запроса и слов 
	содержимого сайта к базовой форме.
* **Возможность указать контекст поиска.** То есть, возможность самостоятельно выбрать 
	контент сайта, в пределах которого будет работать поисковый алгоритм, а также определить 
	значимость для каждого из пределов. Например, рассмотрим интернет-магазин. Предполагается, 
	что поисковый запрос чаще всего будет содержать название искомой продукции, поэтому поиск по 
	названиям товара будет иметь наивысший приоритет. В качестве следующего приоритета можно 
	выбрать поиск по свойствам товаров, затем поиск по описанию.
* **Индексирование содержимого сайта.** Представьте ситуацию: одновременно около 30 человек 
	выполняют поисковые запросы. Сервер принимает каждое соединение, управление потоком 
	передается интерпретатору PHP. При каждом запросе заново инициализируется поисковый 
	движок, заново перерывается содержимое сайта... Сложно сказать, сколько времени и 
	ресурсов потребуется, чтобы обработать все эти запросы. Именно для того, чтобы не 
	делать одну и ту же работу по сто раз, была придумана технология индексирования. 
	Индексирование выполняется только при изменении или добавлении содержимого сайта, 
	а поиск выполняется уже по индексу, а не по содержимому.
* **Механизм ранжирования.** Ранжирование результатов поиска - это сортировка результатов поиска, выполняемая на основе оценки значимости найденных данных. Например, в каком-нибудь блоге выполняется поисковый запрос "космос". Данное слово содержится в двух статьях: в первой 16 раз, во второй - 5 раз. Вероятнее всего, первая статья будет иметь большее значение для инициатора поиска. Также каждой разновидности содержимого сайта при индексировании задается определенный коэффициент, который будет влиять на его позиции в поисковой выдаче.

Описание репозитория еще дорабатывается, все подробности и примеры использования можно найти тут:
[http://habrahabr.ru/post/244561/](http://habrahabr.ru/post/244561/)