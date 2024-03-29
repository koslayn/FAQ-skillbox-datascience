# Интересная статистика и опросы:
На 14 июля 2020:
  * Две курсовые по аналитике сдали около 200 студентов;
  * Курсовую по ML - около 25.

На 17 августа 2020:
  * Две курсовые по аналитике сдали около 250 студентов;
  * Курсовую по ML - около 40.

# Разное, полезное, интересное.
* [👨‍🎓️📊 Как научиться Data Science онлайн: 12 шагов от новичка до профи](https://proglib.io/p/kak-nauchitsya-data-science-onlayn-12-shagov-ot-novichka-do-profi-2020-06-30)
* [Руководство для начинающих - ML BootCamp](https://mlbootcamp.ru/ru/article/tutorial/)
  > **Alexander Kamyshnikov:** ... статья - подробно с примерами от загрузки данных, их трансформации, преобразования, очистки до обучения и получения результатов

# Запуск Jupyter Lab в Docker
* Уставновить Docker - для этого, включить виртуализацию в BIOS, в Windows включить WSL2 или Hyper-V.
  * WSL2 - более новая и должна работать лучше, но установка чуть сложнее и состояние beta, работает начиная с windows 2004.
  * Проще пока (на конец июля 2020) включить Hyper-V.
* `docker pull jupyter/datascience-notebook` - получаем докер файл. Есть различные готовые [образы с различным набором библиотек](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html)
* Подключить папку для доступа из Docker. [Вот инструкция, но возможно не обязательно делать.](https://rominirani.com/docker-on-windows-mounting-host-directories-d96f3f056a2c).
* [Подробная инструкция по Docker и Jupyter Lab](https://www.dataquest.io/blog/docker-data-science/).  

Основное (запуск происходит вот такой командой):
  
`docker run --rm -p 8888:8888 -e JUPYTER_ENABLE_LAB=yes -v "//D/DataScientist:/home/jovyan/work" jupyter/datascience-notebook`
  * `--rm` - "очистить" контейнер после выключения (все на заводские).
  * `-p 8888:8888` - связать порт локального компьютера и порт Docker-контейнера.
  * `-v //D/DataScientist:/home/jovyan/work` - связать директорию локального компьютера и контейнера
    * `//D/` - замена пути для windows `D:\`
    * `:` - соединитель путей
    * `/home/jovyan/work` - рабочая директория контейнера (задана его создателями)
    * `"..."` - кавычки не обязательны, если нет пробелов в пути к нужной папке
  * `jupyter/datascience-notebook` - какой контейнер запускать.
  * В консоли будет ссылка, по которой можно будет подключится к Jupyter Lab
* Если не хватает пакетов в контейнере можно их доставить
  * `docker ps` - когда контейнер работает покажет его ID
  * `docker exec 06b8394227e1 pip install requests`
    * `exec` - выполнить команду в контейнере
    * `06b8394227e1` - id контейнера
    * всё что после `docker exec 06b8394227e1` - просто команды которые передаются в консоль контейнера
* Установленное не сохранится после выключения контейнера, можно собрать контейнер под себя, с этим нужно разбираться.

# Jupyter lab - Git - версионирование блокнотов
Для Jupyter lab есть плагин, который позволяет работать с git.
Плагин и инструкция по установке выложены на [github:  jupyterlab /
jupyterlab-git](https://github.com/jupyterlab/jupyterlab-git)
Также можно поставить из репозитория Anaconda:
```
conda install jupyterlab-git
jupyter lab build
```
Для анаконды возможно придётся подключить сторонний репозиторий `conda-forge` - `conda config --add channels conda-forge`