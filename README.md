# Пример проекта "Микросервиса по учету и сортировке товара" Spring Boot
Это образец приложения Java / Maven / Spring Boot (версия 2.5.6), которое можно использовать в качестве шаблона для построения микросервиса по учету и сортировке товара, например, товара на складе.
## О сервисе
Данное приложение представляет собой REST-сервис для просмотра и взаимодействия с товарной базой. В качестве примера за товар взяты носки (с параметрами цвет, количество, содержание хлопка в %). Вот на что способно это небольшое приложение:
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
/api/socks
/api/socks/income
/api/socks/outcome
/api/socks/{id}

```
### испоьзуемые технологии          
* Spring Data JPA
* Spring Boot Starter
* ModelMapper
* Lombok
* mysql

            
           
       




# Вопросы и комментарии:  kapcap96@yandex.ru
