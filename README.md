Тестовое задание
Цель
Создать приложение на Django REST Framework, которое будет обрабатывать POST-запросы, принимая данные с удалённого модема и создавая соответствующие сущности в базе данных, а также реализовать возможность получения этих сущностей через GET-запросы.
Задание
1.	Создайте Django проект с приложением:
o	Используйте Django REST Framework для разработки API.
2.	Создайте модель данных:
o	Разработайте модели для следующих сущностей: 
	Modem: для хранения информации о модеме (например, MAC-адрес).
	Sensor: для хранения информации о датчиках (MAC-адрес, вибрация и температура).
	Counter: для хранения данных счётчиков электроэнергии.
3.	Реализуйте API:
o	Реализуйте один POST-эндпоинт, который будет принимать данные в следующем формате: {
    
4.	Реализуйте GET-эндпоинты:
o	Реализуйте GET-эндпоинты для получения сущностей: 
	Получение списка всех модемов.
	Получение списка всех датчиков.
	Получение списка всех счётчиков.
5.	Логика обработки данных:
o	При получении POST-запроса приложение должно: 
	Создавать или обновлять запись о модеме на основе его MAC-адреса.
	Создавать или обновлять записи о датчиках (вибрации и температуры) на основе их MAC-адресов и значений.
	Создавать записи о счётчиках с соответствующими данными.
6.	Docker и PostgreSQL (дополнительно):
o	Если возможно, реализуйте проект с использованием docker-compose, чтобы поднять PostgreSQL в контейнере.
o	Убедитесь, что ваше приложение может взаимодействовать с PostgreSQL, запущенной в контейнере.
7.	Тестирование:
o	Напишите модульные тесты для проверки работы вашего API: 
	Убедитесь, что данные корректно сохраняются в базе данных.
	Проверьте обработку ошибок (например, некорректные данные).
Ожидаемые результаты
•	Полный проект Django, включающий модели, сериализаторы и представления.
•	API, который корректно обрабатывает указанный POST-запрос и сохраняет данные в базе данных.
•	Реализованные GET-эндпоинты для получения сущностей.
•	Модульные тесты для проверки функциональности.
•	(Дополнительно) Конфигурация docker-compose для запуска PostgreSQL.


Для запуска приложения: 
docker-compose up --build

API доступно по адресу localhost:7777

POST-эндпоинт: /api/add_or_update/

GET-эндпоинты:

/api/all_modems/

/api/all_sensors/

/api/all_counters/


