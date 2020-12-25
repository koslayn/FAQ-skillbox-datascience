# Data Scientist. Аналитика. Начальный уровень
# Оглавление
* ...

# Module 1. Язык программирования R (часть 1)
Работать с R-studio можно через docker:
* Запускается rstudio и доступно на порту 8787.
* привязывается папка, которая у вас в терминале.
* Запускается контейнер с root доступом.

```bash
docker run -d -p 8787:8787 --name studio -v ${pwd}:/home/rstudio -e ROOT=TRUE -e PASSWORD="rstudio" rocker/rstudio
```

Для подключения к терминалу контейнера можно использовать следующую команду:
```bash
# Потребуется для доустановки libxml2
docker exec -ti studio bash
```

# Module 3. Язык программирования R (часть 3) 

Возможно у вас будут проблемы с установкой библиотеки. Можно попробовать следующие:
```R
update.packages(repos='http://cran.rstudio.com/', ask=FALSE, checkBuilt=TRUE)
install.packages("tidyverse", dependencies = TRUE)
tidyverse_update()
```

Для Linux
```bash
sudo apt-get install libxml2
```