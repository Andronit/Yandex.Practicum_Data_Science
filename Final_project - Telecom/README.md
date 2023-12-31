### Yandex.Practicum-Data-Science

# Прогноз оттока клиентов Телеком - компании

## Описание проекта
Оператор связи «Ниединогоразрыва.ком » хочет научиться прогнозировать отток клиентов. Если выяснится, что пользователь планирует уйти, ему будут предложены промокоды и специальные условия. Команда оператора собрала персональные данные о некоторых клиентах, информацию об их тарифах и договорах. 

## Цель проекта

Построить модель, которая спрогнозирует отток клиентов.

## Признаки
Данные состоят из файлов, полученных из разных источников:

contract_new.csv — информация о договоре;
personal_new.csv — персональные данные клиента;
internet_new.csv — информация об интернет-услугах;
phone_new.csv — информация об услугах телефонии.

Во всех файлах столбец customerID содержит код клиента.

## Целевой признак

* Решение клиента (уйти или остаться)

### Используемые инструменты
`catboost` `lightgbm` `sklearn` `pandas` `numpy` `matplotlib` `plotly` `math` `time` `xgboost` `pipeline` `seaborn`

### Модели
`CatBoostClassifier` `LGBMClassifier` `RandomForestClassifier`

### Дополнительно
`OneHotEncoder` `GridSearchCV` `make_scorer` `cross_val_score`

### Метрики
`roc_auc_score` `accuracy_score` `roc_curve`

### Вывод:

В ходе выполнения работы, мы составили план работ, провели анализ и прдобработку данных, обучение моделей. В ходе анализа мы проверили корреляцию признаков, создали дополнительные признаки (такие как продолжительность договора) и создали целевой признак. После этого мы закодировали данные через ОНЕ кодировщик и приступили к обучению моделей. Использовали 3 модели: случайный лес, lgbm и catboost. Лучше всех результат получили на модели catboost (Roc-Auc: 0.88, Accuracy 0.94). Посмотрели важность признаков в модели catboost. Далее проверили модель catboost на тестовой выборке. Получили результат Roc-Auc: 0.90 и Accuracy 0.92). По графику roc-кривой убедились, что модель выдает не случайные значения.

### План работы:

- Подготовка данных:
* Импорт необходимых библиотек
* Импорт датасетов
* Ознакомление с данными в датасетах и их типами
* Предобработка данных
- Исследовательский анализ данных
- Разделение на обучающую и тестовую выборки
- Обучение моделей (точно не решил, но планирую использовать эти модели):
* Модель логистической регрессии
* Модель случайного дерева
* Модель CatBoost
- Тестирование лучшей модели
- Вывод
- Отчет
