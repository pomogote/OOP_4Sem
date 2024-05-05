# [LR4](https://github.com/pomogote/OOP_4Sem/tree/main/LR4)

### Задание:
>Разработать страницу отображающую список объектов, с хранением их на сервере в БД MySQL WorkBench, передача данных осуществляется по JSON, 
>клиент и сервер общаются по средством передачи данных. Применить шаблон проектирования MVC. На странице предусмотреть форму добавления объектов в список.
> #### Основные условия выполнения
>- Сформировать строку JSON
>- Передать строку JSON на сервер
>- Должно быть не менее 5 свойств у объекта (Например: Список студентов 1 - Имя, 2 - Фамилия,  3- группа, 4 - возраст,  5- изучаемый предмет)
>- Должны быть все четыре элемента CRUD (create-read-update-delete)

### Основные файлы
1. [view.html](https://github.com/pomogote/OOP_4Sem/blob/main/LR4/src/main/webapp/view.html) - страница-интерфейс, с помощью которого пользователь взаимодействует с программой. 
CRUD операции реализованы с помощью ajax запросов. 

2. [Model_library.java](https://github.com/pomogote/OOP_4Sem/blob/main/LR4/src/main/java/com/example/Model_library.java) - модель библиотеки в котром реализованы методы добавления, чтения, обновления и удаления объектов. Из этого класса программа взаимодействует с БД.

3. [Book.java](https://github.com/pomogote/OOP_4Sem/blob/main/LR4/src/main/java/com/example/Book.java) - объект Книга, который кладется в библиотеку и посылается в виде Json.

4. [ControllerServlet.java](https://github.com/pomogote/OOP_4Sem/blob/main/LR4/src/main/java/com/example/ControllerServlet.java) - сервлет-контроллер. 
Через view.html пользователь отправляет информацию на сервлет-контроллер. 
Там информация принимается, обрабатывается, записывается в модель.
Для осуществления CRUD операций реализованы методы doPost, doGet, doPut, doDelete соответственно. 

#### view.html:
![image](https://github.com/pomogote/OOP_4Sem/blob/main/LR4/1.jpg)

#### Удаление объекта:
![image](https://github.com/pomogote/OOP_4Sem/blob/main/LR4/2.jpg)

#### Пустая база данных:
![image](https://github.com/pomogote/OOP_4Sem/blob/main/LR4/3.jpg)

#### Добавление объекта:
![image](https://github.com/pomogote/OOP_4Sem/blob/main/LR4/4.jpg)

#### Изменение объекта:
![image](https://github.com/pomogote/OOP_4Sem//blob/main/LR4/5.jpg)
