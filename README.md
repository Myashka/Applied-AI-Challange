# Applied-AI-Challange
## Oil and Gas Industry Case 2022

__Задание__: _предсказать дебит нефти на нескольких скважинах на основе различных показателей со скважин._

[Baseline от организаторов](https://github.com/Myashka/Applied-AI-Challange/tree/main/baseline)

---
### Работа с данными
__Особенности__:
1. Данные представляли из себя временные ряды;
2. Каждая скважина имела множество пропусков в данных, причем для каждый скважины они были индивидуальные;
3. Было принято решение работать только с теми показателями, информация о которых имелась в более, чем 50% моментов времени, пропуски были линейно интерполированы.

[Ноутбук работы с данными](https://github.com/Myashka/Applied-AI-Challange/blob/main/Data%20exploring.ipynb)

---
### Модель прогнозирования
Было проведено несколько эксперементов, и выбрана авторегрессионная модель на основе _CatBoost_ и _Skforecast_ для автоматического построения признакого пространства и оптимизации модели.

Подбор гиперпараметров осуществлялся с помощью _GrivSearch_.

В качестве baseline модели также был протестирован _RandomForest_.

[Финальный ноутбук с построением предсказаний](https://github.com/Myashka/Applied-AI-Challange/blob/main/CatBoost_forecasting-3.ipynb)

[Все предсказания моделей](https://github.com/Myashka/Applied-AI-Challange/tree/main/Forecasts)

---
### Работа с Prophet
Был использован "пророк" от Facebook для предсказывания верменного ряда.
С начала были предсказаны экзогенные переменные, а далее на основе предсказанных данных, была предсказана целевая метрика.

[Ноутбук с пророком](https://github.com/Myashka/Applied-AI-Challange/blob/main/Prophet_forecasting.ipynb)

___
[Сертификат](https://github.com/Myashka/Applied-AI-Challange/blob/main/certificate.pdf)