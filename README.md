# Домашнее задание к занятию «Базы данных, их типы» - Антипов Николай

# Задание 1. СУБД

## Кейс

Крупная строительная компания, которая также занимается проектированием и девелопментом, решила создать правильную архитектуру для работы с данными. Ниже представлены задачи, которые необходимо решить для каждой предметной области.

Какие типы СУБД, на ваш взгляд, лучше всего подойдут для решения этих задач и почему?

1.1. Бюджетирование проектов с дальнейшим формированием финансовых аналитических отчётов и прогнозирования рисков. СУБД должна гарантировать целостность и чёткую структуру данных.

1.2. Под каждый девелоперский проект создаётся отдельный лендинг, и все данные по лидам стекаются в CRM к маркетологам и менеджерам по продажам. Какой тип СУБД лучше использовать для лендингов и для CRM? СУБД должны быть гибкими и быстрыми.

1.3. Отдел контроля качества решил создать базу по корпоративным нормам и правилам, обучающему материалу и так далее, сформированную согласно структуре компании. СУБД должна иметь простую и понятную структуру.

1.4. Департамент логистики нуждается в решении задач по быстрому формированию маршрутов доставки материалов по объектам и распределению курьеров по маршрутам с доставкой документов. СУБД должна уметь быстро работать со связями.

Приведите ответ в свободной форме.


#### Ответ:

1.1 Для задачи бюджетирования проектов я считаю что стоит выбрать реляционную СУБД с поддержкой транзакций и ACID-свойствами. Так как реляционная СУБД обеспечивает целостность данных и четкую структуру данных. Примеры таких СУБД MSSQL, Oracle и тд

1.2 В данном случае можн овыбрать NoSQL так как основными преимуществами данной СУБД как раз таки и является гибкость и высокая производительность. Например MongoDb

1.3 В данном случае рекомендуется использовать иерархическую СУБД

1.4 В данном случае луче использовать графовую или сетевую NoSQL СУБД


# Задание 2. Транзакции

2.1. Пользователь пополняет баланс счёта телефона, распишите пошагово, какие действия должны произойти для того, чтобы транзакция завершилась успешно. Ориентируйтесь на шесть действий.

Приведите ответ в свободной форме.


#### Ответ:

1. Прочитать сколько у пользователя денег на счёте с которого он пополняет баланс телефона.
2. Уменьшить на количесвто пополняемых рублей
3. Проверить что денег на счёт стало меньше на сумму на которую мы хоттим пополнить счёт телефона.
4. Проверить баланс телефона.
5. Увеличить баланс телефона на сумму пришедшую с счёта пользователя.
6. Проверить, что баланс увеличился на необхождимую сумму


# Задание 3. SQL vs NoSQL

3.1. Напишите пять преимуществ SQL-систем по отношению к NoSQL.

Приведите ответ в свободной форме.


#### Ответ:

1. SQL-системы поддерживают транзакции, что позволяет гарантировать ACID-свойства.
2. SQL-системы используют унифицированный язык запросов, который обеспечивает простоту и гибкость в создании запросов.
3. Весьма распространены и имеют широкубю подержку разрботчиков.
4. Хорошо интегрируются с различными инструментами для бизнес-аналитики
5. У SQL-систем есть множество инструментов для управления и администрирования баз данных.


# Задание 4. Кластеры

Необходимо производить большое количество вычислений при работе с огромным количеством данных, под эту задачу выделено 1000 машин.

На основе какого критерия будете выбирать тип СУБД и какая модель распределённых вычислений здесь справится лучше всего и почему?

Приведите ответ в свободной форме.


#### Ответ:

СУБД будет выбираться на основе критерия распределённых вычислений. Модель распределённых вычислений (MapReduce) используется для параллельных вычислений над очень большими, вплоть до нескольких петабайт, наборами данных в компьютерных кластерах. Так как под задачу будет задействовано 1000 машин, то выбор скорее всего падёт на NoSQL-СУБД, так как они обычно лучше масштабируются горизонтально в сравнении с реляционными СУБД, следовательно можно более эффективно использовать 1000 машин для обработки данных.
