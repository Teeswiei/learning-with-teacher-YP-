# Отток клиентов 
Из «Бета-Банка» стали уходить клиенты. Каждый месяц. Немного, но заметно. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых.


Нужно спрогнозировать, уйдёт клиент из банка в ближайшее время или нет. Вам предоставлены исторические данные о поведении клиентов и расторжении договоров с банком. 


Построить модель с предельно большим значением *F1*-меры. Чтобы сдать проект успешно, нужно довести метрику до 0.59. Проверьте *F1*-меру на тестовой выборке самостоятельно.


Дополнительно измеряйте *AUC-ROC*, сравнивайте её значение с *F1*-мерой.


Источник данных: [https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling](https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling)



__Признаки__
- RowNumber — индекс строки в данных
- CustomerId — уникальный идентификатор клиента
- Surname — фамилия
- CreditScore — кредитный рейтинг
- Geography — страна проживания
- Gender — пол
- Age — возраст
- Tenure — сколько лет человек является клиентом банка
- Balance — баланс на счёте
- NumOfProducts — количество продуктов банка, используемых клиентом
- HasCrCard — наличие кредитной карты
- IsActiveMember — активность клиента
- EstimatedSalary — предполагаемая зарплата

__Целевой признак__
- Exited — факт ухода клиента



__Используемые модели для задачи классификации: DecisionTreeClassifier, RandomForestClassifier, LogisticRegression c использованием апсэмплинга и параметра взвешенных весов с полученными значениями метрик:__

С апсэмплингом:

* DecisionTreeClassifier: f1 = 0.5980498374864571 auc-roc = 0.8432532638176249 
* RandomForestClassifier: f1 = 0.6234718826405868 auc-roc = 0.8654122064266365 
* LogisticRegression: f1 = 0.47451669595782076 auc-roc = 0.7814518861485736

С параметром взвешенных лесов:

* DecisionTreeClassifier: f1 = 0.5980498374864571 auc-roc = 0.8440833021258383
* RandomForestClassifier: f1 = 0.625 auc-roc = 0.8655856714637045 
* LogisticRegression: f1 = 0.4744268077601411 auc-roc = 0.7814275686200126