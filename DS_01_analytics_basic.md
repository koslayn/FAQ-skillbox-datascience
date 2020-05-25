# Data Scientist. Аналитика. Начальный уровень

## Module 12 - Библиотека pandas. Часть 1

### Проблемы в модуле
Проблема с загрузкой данных в формате numpy `"ValueError: Object arrays cannot be loaded when allow_pickle=False"`.  
Решается добавлением ключа: `arr = np.load(file_path, allow_pickle=True)`  
Подробности об ошибке:
* Проблема возникла после версии `numpy==1.16.2`
* `pickle` - модуль сериализации и десериализации данных (Бинарый формат), для повышения безопастности было изменено поведение библиотеки по умолчанию
* [Подробности](https://stackoverflow.com/questions/55824625/how-to-fix-object-arrays-cannot-be-loaded-when-allow-pickle-false-in-the-sketc)
* [Ещё подробности](https://github.com/tensorflow/tensorflow/commit/79a8d5cdad942b9853aa70b59441983b42a8aeb3#diff-b0a029ad68170f59173eb2f6660cd8e0)


## Module 15 - Чтение и запись данных. Часть 1

### Проблемы в модуле

Домашняя работа, часть 4. Работа с данными формата HTML.
Для правильного отображения символов кириллицы потребуется создать объект класса etree.HTMLParser.

`from lxml import html, etree`
`hparser = etree.HTMLParser(encoding='utf-8')`

И добавить его в аргументы:

`html_tree = html.fromstring(page, parser=hparser)`

## Module 16 - Основы SQL

### Проблемы в модуле

Домашняя работа, часть 15.3.3 - Вывести имена трех самых молодых студентов, трех самых старых преподавателей, названия трех самых продолжительных курсов.

Каждое выражение `SELECT , GROUP BY , LIMIT` нужно включить в скобки, в противном случае будет ошибка.

## Module 17 - Чтение и запись данных. Часть 2

### Проблемы в модуле
Проблема в установке `psycopg2`: 
* для Windows нужно делать `pip install psycopg2-binary`, тогда `import psycopg2` заработает.