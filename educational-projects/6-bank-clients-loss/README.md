# Отток клиентов
## Библиотеки
pandas, sklearn
## Описание

Из «Бета-Банка» стали уходить клиенты. Каждый месяц. Немного, но заметно. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых.

Нужно спрогнозировать, уйдёт клиент из банка в ближайшее время или нет. Нам предоставлены исторические данные о поведении клиентов и расторжении договоров с банком.

Построим модель с предельно большим значением F1-меры (выше или равно 0.59).

Дополнительно измерим AUC-ROC, сравнивая её значение с F1-мерой.

Источник данных: https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling

**Статус проекта: закончен**
## Результат проекта
После предобработки данных, было исследовано влияние дисбаланса классов на ключевые метрики классификации, выявлена модель, наиболее чувствительная к дисбалансу классов, а также построена модель с f1-мерой: 0,60