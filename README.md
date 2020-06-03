# Skillbox data science FAQ unofficial

# Оглавление
* [Data Scientist. Аналитика. Начальный уровень](DS_01_analytics_basic.md)
* [Data Scientist. ML. Начальный уровень](DS_01_ML_basic.md)
* [Основы математики для Data Science](DS_01_math.md)

Не официальный FAQ по курсу Data Science
**Создан для:**
* практики совместной работы,
* практики работы с git,
* сбора полезных материалов, которые теряются в чате-курса.
* ...
* другое, придумаем в процессе :)

**Как читать FAQ:**
* Открывать можно и просто в браузере или приложении github.
* Если хотите попрактиковаться с git, то вам нужно установить [приложение](https://git-scm.com/downloads)
* После запустить git-bash (командная строка) и перейти в папку, в которой вы хотите расположить репозиторий (файлы)
  * В windows можно использовать контекстное меню (правая кнопка мыши в папке - "Git Bash Here")
  * [Как работать с bash](https://tproger.ru/translations/bash-cheatsheet/)
  * Основные команды:
    * `cd folder_name` - перейти в папку (TAB - авто дополнение)
    * `cd..` - подняться на уровень выше.
    * `ls` - показать файлы в папке
* Ввести команду: `git clone https://github.com/koslayn/datascience.git` - это сделает копию репозитория на ваш компьютер.
* Для того, чтобы получить обновления нужно ввести `git pull` - находясь в той папке, где расположен репозиторий.

**Как участвовать в наполнение репозитория:**
* Есть так называемые `pull request` - они позволяют добавлять изменения тем, кто не является контрибьютором, но они устроены достаточно сложно - по этому проще всего всех желающих пригласить в контрибьюторы.
* **Напишите в телеграмме и я добавлю вас (мне нужен будет ваш ник на github).**

**Как сделать изменения и добавить новые материалы в FAQ:**
* `git pull` - получить все изменения из репозитория.
* `git add .` - эта команда добавить то что вы изменили в индекс (зафиксирует состояние файлов).
* `git commit -m 'Сообщение'` - создаст коммит (об этом рассказывал Вадим в лекциях) - подготовка данных к отправке.
* `git push` - отправит ваши изменения в репозиторий.
* если это сложно можете попробовать сделать это через графический интерфейс см. ниже.

[Также в git есть GUI пример работы](https://www.youtube.com/watch?v=kzLz5E486Pk)
[GIT - быстрый старт](https://tproger.ru/translations/git-quick-start/)
[GIT - подробная инструкция](https://tproger.ru/translations/beginner-git-cheatsheet/)

**Правила наполнения  FAQ:**
* Пока никаких не придумано, но давайте только не будем выкладывать домашние задания.
* Если что-то сломается, всегда можно будет откатить, по этому не бойтесь добавлять ваши правки.
* Предлагаю все офорлять при помощи [Markdown](https://guides.hexlet.io/markdown/) и элементами HTML.
* Код можно писать как в конспекты, так и оформлять в виде `.py` b `ipynb` и делать ссылки на них.
  
Например - вот `<pre></pre>` - можно оформлять код:
<pre>
for i in my_list:
    print(i)
</pre>
