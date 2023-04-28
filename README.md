# VKR
Аттестационная работа МГТУ Баумана
Цель создания данного проекта является разработка моделй машинного обучения для создания композиционных материалов с улучшенными характеристиками.
Данные предоставлены в виде excel-таблиц (каталог data_composite):
Таблица «X_bp.xlsx»;
Таблица «X_nup.xlsx»
Для разработки использовались библиотеки pandas, numpy, matplotlib.pyplot, seaborn, sklearn.
Созданы и обучены модели с помощью моделей регрессии и нейронной сети.

Результаты анализа данных.
- данные не взаимосвязаны (корреляция очень слабая)
- введение доп параметра "удельная прочность" не позволил выявить зависимости между переменными 

Разработанные модели дают результаты хуже, чем если просто брать среднее значение прогнозируемой величины. 
- Если данные не нормализовать, то прогнозные значения все равны при построннии модели "Соотношение матрица-наполнитель".
- но как в первом, так и во втором случае прогнозные значения лежат в пределах 2-3,5 в горизонтальной плоскости.

Таким образом можно сказать, что полученные результаты не позволяют спрогнозировать/предсказать требуемые параметры.
Возможные пути решения - разделить массив данных на несколько схожих групп и провести прогнозирование на них. Например провести кластеризацию по искуственному параметру "удельная прочность".

P.S.: также остается вопрос к качеству данных. Хоть они и были вычещены на предмет выбросов, сами данные имеют слишком большую вариативность. Возможно, данные были собраны при проведении экспериментов в разных условиях (без контроля условий / критериев сбора данных) либо для большого количества материалов с разными физическими свойствами.
