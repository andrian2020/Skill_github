# Проект: Компьютер говорит "НЕТ"




## Задача проекта:
#### На основе данного датасета построить скоринговую модель предсказания дефолта клиентов банка.

## Реализация:
- Провден анализ данных.
- С помощью визуализации удалось определить и исправить смещение распределения некоторых признаков.
- Бинарные признаки и категориальные обработаны с помощью Label Encoder и pd.get_dummies. 
- В качестве модели обучения выбрана логистическая регрессия.
- Посторена наивная модель.
- Вычислены метрики: f1, roc_auc, confusion_matrix
- Проведен feature_engineering
- Модель доработана.
- Проведена регуляризация.
- Снова вычислены метрики.
- Балансировка категорий.
- Снова вычислены метрики.




## В результате можно сделать вывод:


>  Работа с признаками, очистка, feature > > > >engineering,
> дают больше результатов чем настройка >параметров модели, регуляризация и др. 
>Качество модели прежде всго обеспечивается >качественными данными.
>Метрики улучшаются на сотые доли. Единственный >большй прорыв получился после балансировки >категорий.
Для улучшения метрик можно было бы еще попробовать:

Поиграть с гиперпараметрами. Вернуться к анализу признаков и попробовать их изменить.
Например, созданные числовые признаки с датами (сезон, день недели...)
перевести в категориальные и сделать дамми переменные и т.д.
Изменить модель обучения и попробовать другие виды
На текущий момент оставлю в таком виде и возьму последнюю модель лучшими показателями.

