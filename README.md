# Data science | Project : "Spotify"

## Гайд по проекту

Перед началом:
- "README.txt" - Содержит сам проект с визуализациями. Предпологаеться что читатель и будет смотреть его как основной файл на входе.
- "DataFrames" - Содержит в себе все дата сеты.
- "Images" - Содержит в себе все картинки "README.txt".
- "Code_Visual" - Содержит в себе код для всего визуала.
- "Code_Regression" - Содержит в себе сам алгоритм регресии.

p.s. Во всём коде дополнительно были сделаны заметки для удобства чтения и понимания.

## Разделы

- Введение
- Задача
- Exploratory Data Analysis (Анализ данных, более подробно можно просмотреть в Code_Visuals.py)
  - Корреляции
  - Самые популярные десятилетия
  - Самые популярные треки
  - Особенности треков по годам
  - Loudness
- Регрессия
- Итог
- Источники

## Введение

Spotify — интернет-сервис потокового аудио (стриминговый), позволяющий легально прослушивать музыкальные композиции, аудиокниги и подкасты, не скачивая их на устройство. Доступен в виде веб-сайта, приложений для всех операционных систем, смартфонов, смарт-устройств и медиа-систем автомобилей. 

### Данные

Файл «data.csv» содержит более 175 000 песен, собранных с помощью Spotify Web API, а также вы можете найти данные, сгруппированные по исполнителю, году или жанру в разделе данных.

![alt text](https://github.com/Aettio/DS_Project_Spotify/blob/main/Images/Spotify_intro.jpg)

## Задача

Свободный анализ и практика с библиотекой xgboost.

## EDA (Exploratory Data Analysis)

В этом разделе мы выделить основные зависимости и взаимосвязи. Также нужно убедится в том что они имеют смысл. Для начала анализа мною был выбран график для визуализации корреляций.

### Корреляции

Тут можно заметить очень много интересных взаимосвязей которые стоит проверить. В основном нас интересуют корреляции с "year".

![alt text](https://github.com/Aettio/DS_Project_Spotify/blob/main/Images/Корреляции.png)

### Самые популярные десятилетия

Как показали данные треки 90х и 00х годов были и есть самыми популярными десятилетиями и они принесли в мир многие песни которые и по сей день считают своеобразной классикой музыкального жанра.

![alt text](https://github.com/Aettio/DS_Project_Spotify/blob/main/Images/Популярнгсть_по_десятилетиям.png)

### Самые популярные треки

Тут получилось достаточно занятно, мы имеем топ из рождественских треков которые считаются классикой и видимо из-за их повтора на ежегодной основе они умудряются держать топовые позиции на протяжении стольких лет.

![alt text](https://github.com/Aettio/DS_Project_Spotify/blob/main/Images/Самая_популярная_песня.png)

### Особенности треков по годам

Как можно заметить с годами приобретали популярность инные направления музыки которые были более энергичными и танцевальными.

![alt text](https://github.com/Aettio/DS_Project_Spotify/blob/main/Images/Особенности_по_year.jpeg)

### Loudness

Как можно заметить с годами треки становяться всё громче, судя по корреляции это в основном связанно с большей популярность жанров в которых фигурирую "energy" и "dancebility" в следствии чего и "Loudness" показывает рост.

![alt text](https://github.com/Aettio/DS_Project_Spotify/blob/main/Images/loudness_by_year.jpeg)

## Регрессия

Тут всё по стандарту, после разбития выборки на тренировочную и тестовую, тренируем на выбранных данных. Затем предсказываем нашу тестовую выборку "Y test". После чего выводим Model Score +- 74 и Cross Value Score +- 72.
(Более подробно в Code_Regression.py)

## Итог

## Источники

- Датасет : https://www.kaggle.com/yamaerenay/spotify-dataset-19212020-160k-tracks
- xgboost документация https://xgboost.readthedocs.io/en/latest/python/python_api.html#module-xgboost.core
