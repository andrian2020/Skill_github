# Проект: Выбираем авто выгодно.




## Задача проекта:
####  создать модель, которая будет предсказывать стоимость автомобиля по его характеристикам.

## Реализация:
- Написан код для парсинга данных объявлений авто с сайта auto.ru
- Полученные данные очищены, на их основе сформирован датасет для обучения моделей.
- Проведен анализ тестового датасета( по которому нужно предсакзывать стоимость) и полученного с помощью парсинга. Данные объединены в один датасет по общим признакам. 
- EDA: мы выяснили основные зависимости между признаками, признаки разделены на категориальные и числовые, с помощью feature engineering сформированы новые
- В качестве наивной модели обучения выбрана линейная регрессия.
- Посторена наивная модель.Вычислениа метрика MAPE, по ней мы будем оценивать модели построенные в дальнейшем.
- Построены модели на основе алгоритмов CatBoost, GradientBoosting,RandomForest, Стекинг
- Произведен подбор гиперпараметров для различных моделей
- Лограифмирование целевой переменной привело к улучшению результата
- Значительноuj улучшения результата соревнования на kaggle удалось добиться за счет введения понижающего коэффициента (средняя цена б.у автомобиля выросла с момента создания тестового датасета)





## В результате можно сделать вывод:
1. В ходе проекта мне удалось реализовать парсинг достаточно большого объема данных сайта auto.ru. Порядка 219 000 позиций. К сожалению после очистки данных и удаления дубликатов объявлений(их оказалось чень много) у меня остался достатчно небольшой набор данных для трейна порядка 30 000 строк. Думаю, при наличии большего количества времени и ресурсов я получил бы больше данных для обучения моделей, хотя бы в 3-4 раза больше чем тестовый датасет, и это бы положительно сказалось на качестве моделей обучения. Можно было бы еще улучшить метрику.
 2. При парсинге данных изначально не заложил такие признаки как 'ПТС','numberOfDoors', 'vendor'(потом было поздно). Большее количество признаков так же бы улучшило предсказания.
 3. При моделировании удалось понять, что специализированные билиотеки при подборе гиперпараметров дают намного лучшие результаты.
 4. Результат в большей степени зависит от качества данных. Следует больше времени уделять сбору, очистке данных, feature engineering. Это, вместе с выбором правильной модели, в конечном итоге даст больший результат чем настройка гиперпараметров. С помошью улучшения качества данных можно получить улучшение предсказаний моделирования на порядок, в то время как точная подстройка даст проценты или же доли процентов улучшения.
 5. Цель проекта достигнута. Построена модель, способная предсказывать стоимость автомобилей с ошибкой MAPE = 13.28%
