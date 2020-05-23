# Data Scientist. Аналитика. Начальный уровень

## Module 12 - Библиотека pandas. Часть 1

### Проблемы в модуле
Проблема с загрузкой данных в формате numpy `"ValueError: Object arrays cannot be loaded when allow_pickle=False"`.  
Решается добавлением ключа: `arr = np.load(file_path, allow_pickle=True)`
  * Бинарый формат Pickle - хранение и передача объектов в Python.