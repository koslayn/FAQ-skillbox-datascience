# Data Scientist. Аналитика. Начальный уровень

## Module 12 - Библиотека pandas. Часть 1

### Проблемы в модуле
Проблема с загрузкой данных в формате numpy `"ValueError: Object arrays cannot be loaded when allow_pickle=False"`.  
Решается добавлением ключа: `arr = np.load(file_path, allow_pickle=True)`
  * Бинарый формат Pickle - хранение и передача объектов в Python.


## Module 15 - Чтение и запись данных. Часть 1

### Проблемы в модуле

Домашняя работа, часть 4. Работа с данными формата HTML.
Для правильного отображения символов кириллицы потребуется создать объект класса etree.HTMLParser.

`from lxml import html, etree`
`hparser = etree.HTMLParser(encoding='utf-8')`

И добавить его в аргументы:

`html_tree = html.fromstring(page, parser=hparser)`

## Module 16 - Основы SQL.

### Проблемы в модуле

Домашняя работа, часть 15.3.3 - Вывести имена трех самых молодых студентов, трех самых старых преподавателей, названия трех самых продолжительных курсов.

Каждое выражение `SELECT , GROUP BY , LIMIT` нужно включить в скобки, в противном случае будет ошибка.