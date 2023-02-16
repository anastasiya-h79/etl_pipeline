Учебный проект курса "Симулятор аналитика" от karpov.courses.


DAG в airflow, который считается каждый день за вчера. 

1. Параллельно обрабатываем две таблицы. В feed_actions для каждого юзера считаем число просмотров и лайков контента. В message_actions для каждого юзера считаем, сколько он получает и отсылает сообщений, скольким людям он пишет, сколько людей пишут ему. Каждая выгрузка - в отдельном таске.

2. Далее объединяем две таблицы в одну.

3. Для этой таблицы считаем все эти метрики в разрезе по полу, возрасту и ос. Делаем три разных таска на каждый срез.

4. И финальные данные со всеми метриками записываем в отдельную таблицу в ClickHouse.

5. Каждый день таблица дополняется новыми данными. 
