# Data Scientist. Аналитика. Начальный уровень
# Оглавление
* Module 1. Язык программирования R (часть 1)
* Module 3. Язык программирования R (часть 3) 
* Module 5. AB-тестирование. Часть 1
* Module 6. AB-тестирование. Часть 2

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

# Module 5. AB-тестирование. Часть 1
В python нужно будет загружать данные из csv, можно обойтись без pandas
```python
# Читаем текстовый файл
    # Указываем разделитель - запятую
    # Пропускаем заголовок
    # Читаем 2 столбец - OLD, NEW - третий столбец
OLD = np.genfromtxt("conversion.csv", delimiter=",", skip_header=1, usecols=1)
```

# Module 6. AB-тестирование. Часть 2
В python в текущей версии библиотеки есть выбор какую гипотезу тестируем
```python
# The alternative hypothesis can be either two-sided or one of the onesided tests, smaller means that the alternative hypothesis is ``prop < value`` and larger means ``prop > value``.
# In the two sample test, smaller means that the alternative hypothesis is ``p1 < p2`` and larger means ``p1 > p2`` where ``p1`` is the proportion of the first sample and ``p2`` of the second one.

z_stat, p_value = proportions_ztest(count, nobs, alternative='smaller')
```