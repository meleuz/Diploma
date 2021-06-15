# Дипломный проект по курсу «Тестировщик ПО»

## О проекте

В рамках данного проекта необходимо автоматизировать тестирование комплексного сервиса покупки тура, взаимодействующего с СУБД и API Банка.

База данных хранит информацию о заказах, платежах, статусах карт, способах оплаты.

Покупка тура возможна с помощью карты и в кредит. Данные по картам обрабатываются отдельными сервисами (Payment Gate, Credit Gate)

Полные условия и исходные данные описанного кейса можно посмотреть [здесь](https://github.com/netology-code/qa-diploma)

## Документация:

[План автоматизации](https://github.com/meleuz/Diploma/blob/master/Plan.md)

### Запуск тестов:

#### Работа с базой данных MySQl

1. 'docker-compose up -d' - *запуск контейнеров*
   
2. 'java -jar ./artifacts/aqa-shop.jar' - *запуск приложения*
   
3. 'gradlew clean test' - *запуск автотестов*
   
4. 'gradlew allureReport', 'gradlew allureServe' - *создание отчета Allure*

#### Работа с базой данных PostgreSQL

1. 'docker-compose up -d' - *запуск контейнеров*
   
2. 'java -jar ./artifacts/aqa-shop.jar --spring.datasource.url=jdbc:postgresql://localhost:5432/app' - *запуск приложения*

3. 'gradlew clean test -Ddb.url=jdbc:postgresql://localhost:5432/app'- *запуск автотестов*

4. 'gradlew allureReport', 'gradlew allureServe' - *создание отчета Allure*
