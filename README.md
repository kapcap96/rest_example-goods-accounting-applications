# Пример проекта "Микросервиса по учету и сортировке товара" Spring Boot
Это образец приложения Java / Maven / Spring Boot (версия 2.5.6), которое можно использовать в качестве старта для создания микросервиса по учету и сортировке товара, например, товара на складе. Надеюсь, это вам поможет.
## О сервисе
Данное приложение представляет собой REST-сервис для просмотра и взаимодействия с товарной базы. В качестве примера за товар взяты носки (с параметрами цвет, количество, содержание хлопка в %). Вот на что способно это небольшое приложение:
* Написание службы RESTful с использованием аннотации запроса / ответа JSON; просто используйте желаемый``Accept`` заголовок в своем запросе.
* Интеграция Spring Data* с JPA / Hibernate с помощью всего нескольких строк конфигурации и знакомых аннотаций. 
* В приложении используется ДТО модели, что позволяет скрыть ненужную информацию, например, как ``id``.
* Также в приложении  используется библиотеке ``Lombok``, что позволяет существенно сократить количество ненужных строк.
* Использование своих аннотаций ``@OperationType`` и ``@SocksColor``, что позволяет сделать структуру приложения читабельной и простой в восприятии. 
* На данный момент сервис выполняет две функции: 
1)	добавление товара 
2)	изменение товара (если товар с данными параметрами уже существует, то увеличивается/уменьшается его количество)
3)	удаление товара 
4)	просмотр всего товара
5)	сортировка товара по следующим параметрам: цвет товара, количество хлопка в %, количество товара.

Например, Вы можете отсортировать все красные носки с содержанием хлопка меньше/больше/равное 50% 

### Конфигурация системы
```
http://localhost:8080//api/socks
http://localhost:8080/api/socks/income
http://localhost:8080/api/socks/outcome
http://localhost:8080api/socks/{id}

```
### Зависимости используемые в проекте 

```
<dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-data-jpa</artifactId>
            <version>2.5.6</version>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>
        <dependency>
            <groupId>org.modelmapper</groupId>
            <artifactId>modelmapper</artifactId>
            <version>2.4.4</version>
        </dependency>
        <dependency>
            <groupId>org.projectlombok</groupId>
            <artifactId>lombok</artifactId>
            <version>1.18.22</version>
            <scope>provided</scope>
        </dependency>
        <dependency>
            <groupId>mysql</groupId>
            <artifactId>mysql-connector-java</artifactId>
            <version>8.0.25</version>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-test</artifactId>
            <version>2.5.6</version>
            <scope>test</scope>
        </dependency>
```



# Вопросы и комментарии:  kapcap96@yandex.ru
