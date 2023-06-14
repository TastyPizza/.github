<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->

## Tasty Pizza
С помощью приложения клиенты смогут выбрать пиццу, закуски и напитки из меню, оформить заказ и получить уведомление, когда он будет готов. Забрать заказ клиент может в любой точке сети.

### Цели
* Сделать удобным способ заказа пиццы клиентами через мобильное приложение. Это позволит избежать очередей, а также увеличит количество заказов, доходность и повысит лояльность клиентов.
* В приложении можно будет просматривать заказы от лица обычного пользователя и от лица администратора. Администратору доступны функции просмотра заказов клиентов и изменение их статусов.


### Задачи
- [x] Составить спецификацию требований программного обеспечения
- [x] Выстроить архитектуру 
- [x] Разработать сервисы регистрации, профиля, меню и заказов
- [x] Протестировать разработанный функционал

### Архитектура
![alt text](https://github.com/TastyPizza/.github/blob/main/assets/%D0%90%D1%80%D1%85%D0%B8%D1%82%D0%B5%D0%BA%D1%82%D1%83%D1%80%D0%B0.jpeg)

### Сервисы 
* [`Клиентское приложение`](https://github.com/TastyPizza/tasty-pizza-client) 
* [`Профиля и регистрации`](https://github.com/TastyPizza/profile-service.spring) для регистрации новых пользователей 
* [`Меню и заказов`](https://github.com/TastyPizza/menu-orders-service) для отображения меню ресторванов и для выполнения заказов от клиентов

### Вспомогательные сервисы
* [`Api Gateway`](https://github.com/TastyPizza/api-gateway) для перенаправления запросов на необходимые сервисы и авторизации пользователя
* [`Регистрации сервисов`](https://github.com/TastyPizza/service-discovery) (Eureka) для регистрации сервисов 

### Использованные технологии 
* `Spring Boot` (Security, Cloud, Data) на Kotlin
* `RabbitMQ` для общения микросервисов друг с другом 
* `Redis` для кэширования входящих сообщений на api gateway
* `Grafana` для сбора и визуализвции статистики
* `Docker` для контенеризации и внедрения
* `Github Actions` для сбора образов и выгрузки в Docker Hub
* `AndroidX` для андроид приложения
* `Junit` для тестирования разработанного функционала

### Запуск 
Для запуска бэкенда установите [`docker-compose.yml`](https://github.com/TastyPizza/.github/blob/main/assets/docker-compose.yml) и выполните команду `docker compose up`

