# [LR2](https://github.com/pomogote/OOP_4Sem/tree/main/LR2)

### Задание:
>Разработать страницу отображающую список объектов, с хранением их на сервере в файле, 
>передача данных осуществляется по JSON, клиент и сервер общаются по средством передачи данных. 
>На странице предусмотреть форму добавления объектов в список.
> #### Основные условия выполнения
>- Сформировать строку JSON
>- Передать строку JSON на сервер
>- Должно быть не менее 5 свойств у объекта (Например: Список студентов 1 - Имя, 2 - Фамилия,  3- группа, 4 - возраст,  5- изучаемый предмет)
>- Записать полученную строку в файл на сервере

### Основные файлы
1. [main.html](https://github.com/pomogote/OOP_4Sem/blob/main/LR2/src/main/webapp/main.html) - страница с таблицей объектов и формой добавления новых объектов
2. [BookServlet.java](https://github.com/pomogote/OOP_4Sem/blob/main/LR2/src/main/java/com/example/BookServlet.java) - сервлет, в котором информация обрабатывается, записывается в файл и высылается клиенту
3. [Book.java](https://github.com/pomogote/OOP_4Sem/blob/main/LR2/src/main/java/com/example/Book.java) - создан для обработки объектов 

main.html:
![image](https://github.com/pomogote/OOP_4Sem/blob/main/LR2/1.jpg)
Добавлние нового объекта:
![image](https://github.com/pomogote/OOP_4Sem/blob/main/LR2/2.jpg)
![image](https://github.com/pomogote/OOP_4Sem/blob/main/LR2/3.jpg)

library.txt:

![image](https://github.com/pomogote/OOP_4Sem/blob/main/LR2/4.jpg)

### Коментарии к коду [BookServlet](https://github.com/pomogote/OOP_4Sem/blob/main/LR2/src/main/java/com/example/BookServlet.java)
1. Метод init. При запуске сервера в список List<Book> library выгружаются данные из БД (файла library.txt)

2. Метод doGet загружает информацию о книгах из файла library.txt на сервере и отправляет ее в формате JSON клиенту для отображения на странице main.html.

3. Метод doPost обрабатывает запрос от клиента, добавляет новую книгу в список и отправляет обновленную информацию о книгах в формате JSON обратно на клиентскую сторону.
