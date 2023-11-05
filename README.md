# Обнаружение каверов музыкальных треков


[md](https://github.com/MironRodionoff/hackathon_yandex/blob/main/README.md)    
[ipynb](https://github.com/MironRodionoff/hackathon_yandex/blob/main/Project_detection_covers.ipynb)

## Описание проекта

Обнаружение треков каверов - важная продуктовая задача, которая может значительно улучшить качество рекомендаций музыкального сервиса и повысить счастье пользователей. 
Если с высокой точностью классифицировать каверы и связывать их между собой, то можно предложить пользователю новые возможности для управления потоком треков. Например:

* по желанию пользователя можно полностью исключить каверы из рекомендаций;
* показать все каверы на любимый трек пользователя;
* контролировать долю каверов в ленте пользователя.

### Цели проекта:

- Научиться классифицировать треки на каверы и оригиналы
- Построить подходящую модель

### Критерии выполнения проекта:

- Модель обучена и успешно классифицирует треки
- AUC-ROC модели более 0,7
- Accuracy более 0,95

В ходе проекта:

* изучим данные
* проведем предобработку
* подготовим выборки для обучения моделей.
* Преобразуем категориальные признаки для подготовки их к моделированию методом TargetEncoder.
* Стандартизируем диапазон функциональных возможностей входного набора данных с помощью StandardScaler.
* Организуем все эти методы в make_pipeline.
* обучим модели: RandomForestClassifier, XGBClassifier. Соотнесем с константной моделью.
* Для каждой модели подберем наилучшие гиперпараметры с помощью GridSearchCV.
* проанализируем время обучения и предсказания, и качество моделей.
* изучим важность признаков
* выберем лучшую модель, проверим её качество на тестовой выборке.
* Сделаем вывод, включающий:
    - Параметр ROC-AUC и ROC для выбранной модели
    - Параметр accuracy
    

## Навыки и инструменты

- **python**
- **pandas**
- **sklearn**
- **numpy**
- **matplotlib**
- **seaborn**
- **nltk**
- **langid**
- **LightGBM**
- **XGboost**


## Вывод

Лучшие характеристики показала модель **XGBClassifier**
- Значение roc-auc модели: 0.71
- Значение accuracy_score модели: 0.97

Параметры модели:
> n_estimators=1000, 
learning_rate=0.05, 
max_depth=10, 
min_child_weight=3, 
class_weight='balanced'

ROC-кривая показывает нам что преобладающий класс модель предсказывает гораздо лучше. AUC_ROC=0.97.

Для улучшения качества предсказаний можно сделать ресемплинг, дополнить датасет информативными признаками, провести дополнительный подбор гиперпараметров, пересмотреть методы кодирования.

Внедрение предложенной модели поможет бизнесу добавить следующие функции:
* по желанию пользователя можно полностью исключить каверы из рекомендаций;
* контролировать долю каверов в ленте пользователя.

## Участники команды DS:
[Виктория Кузьмина](https://github.com/Viktoriaky)  
[Мирон Родионов](https://github.com/MironRodionoff)  
[Алексей Исаков](https://github.com/IT-DS-Alex)   
Project manager - [Яна Петрова](https://t.me/yana_kalobanova)  
