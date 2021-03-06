[Назад к главной странице курса](https://github.com/db2017ss/syllabus)

## 2. Создание базы данных в СУБД Microsoft Access

### Цель работы

Ознакомление с методами проектирования схемы и управления данными в графическом интерфейсе СУБД Microsoft Access.

### Теоретические сведения

Предварительно ознакомиться: материалы лекции по реляционной модели данных.

Microsoft Access — реляционная СУБД, входящая в пакет Microsoft Office. Для выполнения работы рекомендуется использовать Access версий 2007, 2010, 2013 или 2016.

При выполнении работы необходимо выбрать создание пустой базы данных, а затем по очереди создать все заданные в модели таблицы в режиме конструктора. В этом режиме для каждой колонки указывается имя, тип данных, а также ряд других параметров (размерность, маска ввода, обязательность, пользовательское ограничение).

Пользовательские ограничения (согласно индивидуальному варианту) задаются в поле "Правило проверки" (Access 2013 и Access 2016) или "Условие на значение" (Access 2007 и Access 2010). Синтаксис ограничений описан в [1].

Следует различать ограничения уровня колонки (задаваемые в окне "Свойства поля"), которые проверяются только при занесении или изменении значений в данной колонке, и ограничения уровня таблицы (задаваемые в окне "Свойства таблицы"), которые проверяются при занесении или изменении значений сразу в нескольких колонках.

Ограничение уровня колонки:

![](https://github.com/db2017ss/syllabus/blob/master/img/field_properties.png)

Ограничение уровня таблицы:

![](https://github.com/db2017ss/syllabus/blob/master/img/table_properties.png)

После создания таблиц необходимо перейти к созданию связей между ними, осуществляющих проверку ссылочной целостности. Необходимо помнить, что ссылаться можно только на колонку того же типа, и в целом ссылка (в том числе составная) должна идти на полный ключ.

Для каждой связи помимо указания связанных атрибутов необходимо включать проверку целостности (в противном случае ограничения по внешнему ключу не будут форсироваться), а также (по желанию) каскадное обновление и удаление связанных записей.

![](https://github.com/db2017ss/syllabus/blob/master/img/relationship_properties.png)

Включение каскадное обновления (удаления) активирует режим, когда при изменении (удалении) строки в главной таблице изменяются (удаляются) строки в подчиненной таблице, ссылающуюся на изменяемую (удаляемую) строку.

После завершения работы над схемой данных, можно переходить к заполнению базы данных данными. Помните, что менять схему после занесения в таблицы данных может быть затруднительно. Всего необходимо добавить в таблицы по 5-10 строк, которые правдоподобно и полно отражали бы множественные взаимосвязи между данными.

Также необходимо проверить попыткой внесения некорректных данных, работают ли ограничения ссылочной целостности, заданные связями между таблицами, и пользовательские ограничения.

### План выполнения

1. Реализовать реляционную схему, полученную в ЛР1, визуальными средствами Microsoft Access.
1. Осуществить проверку ограничений в соответствии с индивидуальным вариантом средствами Microsoft Access.
1. Заполнить базу данных данными, позволяющими удостовериться в работоспособности ограничений реляционной модели и пользовательских ограничений.
1. Оформить отчет по проделанной работе.

### Содержание отчета

1. Титульный лист.
1. Цель работы.
1. Индивидуальный вариант задания.
1. Снимок экрана реляционной схемы в Microsoft Access.
1. Тексты логических условий ограничений, заданных для таблиц.
1. Снимки экранов заполненных таблиц и результатов работы ограничений.
1. Выводы.

### Вспомогательные материалы

1. [Создание условия на значение для проверки данных в поле](http://office.microsoft.com/ru-ru/access-help/HA010096312.aspx)

### Вопросы к защите

*   Объясните нотацию реляционной схемы, применяемую в Access.
*   В чем отличие проверок условия на значение на уровне колонки и на уровне таблицы?
*   Объясните принцип работы ограничения X.
*   Что такое потенциальный ключ в реляционной модели?
*   В чем отличие первичного ключа от потенциального ключа?
*   В чем отличие двух потенциальных ключей a и b от составного потенциального ключа (a, b)?
*   Как задать несколько ключей для таблицы в Access?
*   Что такое внешний ключ в реляционной модели?
*   В чем отличие двух внешних ключей a и b от составного внешнего ключа (a, b)?
*   Что означает свойство связи "Обеспечение целостности данных"?
*   Что означает свойство связи "Каскадное обновление связанных полей"?
*   Что означает свойство связи "Каскадное удаление связанных полей"?

[Назад к главной странице курса](https://github.com/db2017ss/syllabus)
