# Task 1.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/1.png)

___

# Task 2.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/2.png)

___

# Task 3.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/3.png)

___

# Task 4.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/4.png)

___

# Task 5.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/5.png)

___

# Task 6.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/6.png)

___

# Task 7.

SELECT *
FROM Wards

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/7.png)

___

# Task 8.

SELECT Surname, Phone
FROM Doctors

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/8.png)

___

# Task 9.

SELECT Floor
FROM Wards
GROUP BY Floor

SELECT *
FROM Wards

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/9.png)

___

# Task 10.

SELECT Name, Severity
FROM Diseases
WHERE Name in ('Виброз','Бульбит') and Severity in (1,2)

SELECT *
FROM Diseases

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/10.png)

___

# Task 11.

SELECT Name Имя, Surname Фамилия, Salary Зарплата
FROM Doctors

SELECT *
FROM Doctors

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/11.png)

___

# Task 12.

SELECT Name
FROM Departments
WHERE Building = 5 and Financing < 30000

SELECT *
FROM Departments

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/12.png)

___

# Task 13.

SELECT Name
FROM Departments
WHERE Building = 3 and Financing > = 12000 and Financing < 15000

SELECT *
FROM Departments

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/13.png)

___

# Task 14.

Вывести названия палат, расположенных в корпусах 4 и 5 на 1-м этаже

SELECT Name
FROM Wards
WHERE Floor = 1 and (Building = 4 or Building = 5)

SELECT *
FROM Wards

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/14.png)

___

# Task 15.

Вывести названия, корпуса и фонды финансирования отделений, расположенных в корпусах 3 или 6 и имеющих фонд финансирования меньше 11000 или больше 25000

SELECT Name, Building, Financing
FROM Departments
WHERE (Building = 3 or Building = 6) and (Financing < 11000 or Financing > 25000)

SELECT *
FROM Departments

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/15.png)

___

# Task 16.

Вывести фамилии врачей, чья зарплата (сумма ставки и надбавки) превышает 1500.

SELECT Surname
FROM Doctors
WHERE Salary + Premium > 1500

SELECT *
FROM Doctors

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/16.png)

___

# Task 17.

Вывести фамилии врачей, у которых половина зарплаты превышает троекратную надбавку.

SELECT Surname
FROM Doctors
WHERE Salary/2 > Premium*3

SELECT *
FROM Doctors

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/17.png)

___

# Task 18.

Вывести названия обследований без повторений, проводимых в первые три дня недели с 12:00 до 15:00.

SELECT Name
FROM Examinations
WHERE DayOfWeek in (1,2,3) and StartTime < = '12:00:00' and EndTime > = '15:00:00'

В условии без повторений, но оно не может повторяться так как Name уникально в таблице

SELECT *
FROM Examinations

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/18.png)

___

# Task 19.

Вывести названия и номера корпусов отделений, расположенных в корпусах 1, 3, 8 или 10.

SELECT Name, Building
FROM Departments
WHERE Building in (1,3,8,10) 

Корпусов в таблице по умолчанию: Должно быть в диапазоне от 1 до 5.(Максимум 5)

SELECT *
FROM Departments

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/19.png)

___

# Task 20.

Вывести названия заболеваний всех степеней тяжести, кроме 1-й и 2-й.

SELECT Name
FROM Diseases
WHERE Severity != 1 and Severity != 2

SELECT *
FROM Diseases

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/20.png)

___

# Task 21.

Вывести названия отделений, которые не располагаются в 1-м или 3-м корпусе.

SELECT Name
FROM Departments
WHERE Building != 1 and Building != 3

SELECT *
FROM Departments

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/21.png)

___

# Task 22.

Вывести названия отделений, которые располагаются в 1-м или 3-м корпусе.

SELECT Name
FROM Departments
WHERE Building in (1,3)

SELECT *
FROM Departments

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/22.png)

___

# Task 23.

Вывести фамилии врачей, начинающиеся на букву “N”.

SELECT Surname
FROM Doctors
WHERE Surname LIKE 'N%';

SELECT *
FROM Doctors

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/23.png)

___

# Task 24.

Вывести таблицу кафедр, но расположить ее поля в обратном порядке.

SELECT [Name],[Financing],[Id]
FROM [Academy].[dbo].[Departments];

SELECT *
FROM Departments;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/24.png)

___

# Task 25.

Вывести названия групп и их рейтинги с уточнением имен полей именем таблицы.

SELECT Groups.Name, Groups.Rating
FROM Groups

SELECT *
FROM Groups;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/25.png)

___

# Task 26.

Вывести для преподавателей их фамилию, процент ставки
по отношению к надбавке и процент ставки по отношению
к зарплате (сумма ставки и надбавки).

SELECT Surname , Premium/Salary [Premium % от зарплаты], Salary/Premium [Salary % от зарплаты]
FROM Teachers;

SELECT *
FROM Teachers;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/26.png)

___

# Task 27.

Вывести таблицу факультетов в виде одного поля в следующем формате: “The dean of faculty [faculty] is [dean].”.

SELECT 'Декан факультета: ' + Name + ' - ' +  Dean [Info]
FROM Faculties 

SELECT *
FROM Faculties;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/27.png)

___

# Task 28.

Вывести фамилии преподавателей, которые являются профессорами и ставка которых превышает 1050.

SELECT Surname
FROM Teachers 
WHERE IsProfessor = 1 and Salary > 1050;

SELECT *
FROM Teachers;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/28.png)

___

# Task 29.

Вывести названия кафедр, фонд финансирования которых меньше 11000 или больше 25000.

SELECT Name
FROM Departments 
WHERE Financing > 11000 and  Financing < 25000

SELECT *
FROM Departments;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/29.png)

___

# Task 30.

Вывести названия факультетов кроме факультета “Computer Science”

SELECT Name
FROM Faculties 
WHERE Name != 'Computer Science';

SELECT *
FROM Faculties;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/30.png)

___

# Task 31.

Вывести фамилии и должности преподавателей, которые не являются профессорами.

SELECT Surname, Position
FROM Teachers 
WHERE IsProfessor = 0;

SELECT *
FROM Teachers;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/31.png)

___

# Task 32.

Вывести фамилии, должности, ставки и надбавки ассистентов, у которых надбавка в диапазоне от 160 до 550.

SELECT Surname, Position, Salary, Premium
FROM Teachers 
WHERE IsAssistant = 1 and Premium >= 160 and Premium < 550

SELECT *
FROM Teachers;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/32.png)

___

# Task 33.

Вывести фамилии и ставки ассистентов.

SELECT Surname, Salary
FROM Teachers 
WHERE IsAssistant = 1;

SELECT *
FROM Teachers;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/33.png)

___

# Task 34.

Вывести фамилии и должности преподавателей, которые были приняты на работу до 01.01.2000.

SELECT Surname, Position
FROM Teachers 
WHERE EmploymentDate < '01.01.2000';

SELECT *
FROM Teachers;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/34.png)

___

# Task 35.

Вывести названия кафедр, которые в алфавитном порядке располагаются до кафедры “Software Development”. Выводимое поле должно иметь название “Name of Department”.

SELECT Name [Name of Department]
FROM Departments 

Вывод до Кафедра разработка программного обеспечения

WHERE Name NOT LIKE 'Кафедра [р-я]%'
ORDER BY Name;

SELECT *
FROM Departments;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/35.png)

___

# Task 36.

Вывести фамилии ассистентов, имеющих зарплату (сумма ставки и надбавки) не более 1200.

SELECT Surname
FROM Teachers 
WHERE IsAssistant = 1 and Premium+Salary < 1200;

SELECT *
FROM Teachers;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/36.png)

___

# Task 37.

Вывести названия групп 5-го курса, имеющих рейтинг в диапазоне от 2 до 4.

SELECT Name
FROM Groups 
WHERE Year = 5 and Rating >= 2 and Rating <= 4;

SELECT *
FROM Groups;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/37.png)

___

# Task 38.

Вывести фамилии ассистентов со ставкой меньше 550 или надбавкой меньше 200.

SELECT Surname
FROM Teachers 
WHERE IsAssistant = 1 and (Salary < 550 or Premium < 200);

SELECT *
FROM Teachers;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/38.png)

___

# Task 39.

SELECT FirstName +' '+LastName AS FullName, Name, D.Id AS DeptIdent
FROM Departaments AS D, Teachers AS T
WHERE T.DepartmentId = D.Id;


![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/39.png)

___

# Task 40.

SELECT FirstName +' '+ LastName AS FullName, Name
FROM Departaments, Teachers
WHERE Teachers.DepartmentId = Departaments.Id;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/40.png)

___

# Task 41.

SELECT FirstName +' '+ LastName AS FullName,
Name AS SubjectName
FROM Teachers AS T, Subjects AS S,
TeachersSubjects AS TS
WHERE T.Id=TS.TeacherId AND S.Id=TS.SubjectId;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/41.png)

___

# Task 42.

SELECT D.Name AS DeptName, S.Name
AS SubjectName
FROM Departaments AS D, Teachers AS T, Subjects
AS S, TeachersSubjects AS TS
WHERE D.Id = T.DepartmentId AND T.Id=TS.
TeacherId AND S.Id=TS.SubjectId;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/42.png)

___

# Task 43.

SELECT D.Name AS DeptName, S.Name
AS SubjectName, FirstName+' '+ LastName AS Teacher
FROM Departaments AS D, Teachers AS T, Subjects
AS S, TeachersSubjects AS TS
WHERE D.Id = T.DepartmentId AND T.Id=TS.
TeacherId AND S.Id=TS.SubjectId;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/43.png)

___

# Task 44.

Вывести количество инструкторов по каждой секции

Select S.Name as [Название секции], COUNT(I.IdSection) as [Количество тренеров]
From Section as S, Instructors as I
where S.Id = I.IdSection
group by I.IdSection, S.Name;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/44.png)

___

# Task 45.

Показать количество людей которые должны заниматься в определённый момент времени в каждой секции

Select S.Name as [Название секции], COUNT(S.Id) as [Количество посетителей]
From Section as S, Visitor as V, 
(Select V.Id as IdVisitor, S.Id as IdSection 
From Visitor as V, Instructors as I, Section as S 
where V.IdInstructor = I.Id and I.IdSection = S.Id and S.TimeStart < '10:00' and S.TimeEnd > '10:00' 
group by V.Id, S.Id) as m
where V.Id = m.IdVisitor and S.Id = m.IdSection
group by S.Id , S.Name;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/45.png)

___

# Task 46.

Вывести количество посетителей фитнес клуба которые пользуются услугами определенного мобильного оператора

SELECT Count(Id) as Kyivstar
FROM Visitor
where Phone LIKE '38098%' or Phone LIKE '38095%'

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/46.png)

___

# Task 47.

получить количество посетителей, у которых фамилия совпадает с фамилиями из определенного списка

SELECT Count(Id) as Count
FROM Visitor
where SurName LIKE 'Лола' or SurName LIKE 'Курочка'

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/47.png)

___

# Task 48.

Показать количество людей с одинаковыми именами которых занимаются у определенного инструктора

Select V.FirstName as [Имя человека], Count(V.FirstName) as [Количество]
From Visitor as V, Instructors as I
Where V.IdInstructor = I.Id and I.Name = 'Роман'
Group by V.FirstName, I.Name

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/48.png)

___

# Task 49.

Получить информацию о людях которые посетили фитнес зал минимальное количество раз

Select FirstName,SurName,Phone
From Visitor,(Select MAX(V.Date) as d From Visitor as V) as D
where Date = D.d

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/49.png)

___

# Task 50.

Вывести количество посетителей, которые занимались в определённой сенкции за первую половину текущего года

Select Count(FirstName) as [количество посетителей]
From Visitor, Instructors as I, Section as S
where IdInstructor = I.Id and I.IdSection = S.Id and S.Name = 'Кардиотренажеры' and Date < '01.06.2021'


![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/50.png)

___

# Task 51.

Определить количество людей посетивших фитнес зал за прошлый год

Select Count(FirstName) as [Количество посетителей за прошлый год]
From Visitor
where year(Date) <= '2020'

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/51.png)

___

# Task 52.

Вывести количество палат, вместимость которых больше 10.

Select Name
From Wards
Where Places > 10

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/52.png)

___

# Task 53.

Вывести названия корпусов и количество палат в каждом из них

Select B.Name, COUNT(W.DepartmentId) as [Counts Place]
From Wards as W, Departments as D, Build as B
Where D.Id = W.DepartmentId and B.Id = D.Building
Group by W.DepartmentId, B.Name

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/53.png)

___

# Task 54.

Вывести названия отделений и количество палат в каждом из них

Select D.Name, COUNT(W.DepartmentId) as [Counts Place]
From Wards as W, Departments as D
Where D.Id = W.DepartmentId
Group by W.DepartmentId, D.Name

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/54.png)

___

# Task 55.

Вывести названия отделений и суммарную надбавку врачей в каждом из них.

Select D.Name as [Отделение], Sum(Premium) as [Суммарная надбавка]
From Departments as D, Doctors as Doc
Where D.Id = Doc.DepartamentsId
Group by D.Name

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/55.png)

___

# Task 56.

Вывести названия отделений, в которых проводят обследования 5 и более врачей.

Select D.Name as [Отделение]
From Departments as D, Doctors as Doc
Where D.Id = Doc.DepartamentsId
Group by D.Name
Having Count(Doc.Name) > 5

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/56.png)

___

# Task 57.

Вывести количество врачей и их суммарную зарплату (сумма ставки и надбавки).

Select Count(Name) as [Количество врачей], Sum(Premium+Salary) as [Сумарная зарплата]
From Doctors

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/57.png)

___

# Task 58.

Вывести среднюю зарплату (сумма ставки и надбавки) врачей.

Select Avg(Premium+Salary) as [Средняя зарплата]
From Doctors

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/58.png)

___

# Task 59.

Вывести названия палат с минимальной вместительностью.

Select Name
From Wards
where Places = (Select Min(Places) From Wards)

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/59.png)

___

# Task 60.

Вывести в каких из корпусов 1, 6, 7 и 8, суммарное количество мест в палатах превышает 100. При этом учитывать только палаты с количеством мест больше 10.

Select Name as [Корпус], S.s as [Количество мест в палатах]
From Build, (Select B.Name as n, Sum(Places) as s
From Departments as D, Build as B, Wards as W
where (B.Id = 1 or B.Id = 6 or B.Id = 7 or B.Id = 8) 
and B.Id = D.Building and D.Id = W.DepartmentId and W.Places > 10
Group by B.Name) as S
where Name = S.n and S.s > 100

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/60.png)

___

# Task 61.

Показать все книги, количество страниц в которых больше 500, но меньше 650

Select Name, Pages
From Books
Where Pages > 500 and Pages < 650

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/61.png)

___

# Task 62.

Показать все книги, в которых первая буква названия либо. «А», либо «З».

Select Name, Pages
From Books
Where Name LIKE 'А%' OR  Name LIKE 'З%';

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/62.png)

___

# Task 63.

Показать все книги жанра «Детектив», количество проданных книг более 30 экземпляров.

Select B.Name
From Books AS B, Themes AS T, Sales AS S
Where T.Name LIKE 'Детектив' AND T.Id = B.ThemeId
AND B.Id = S.BookId AND Quantity > 30

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/63.png)

___

# Task 64.

Показать все книги, в названии которых есть слово «Microsoft», но нет слова «Windows».

Select B.Name
From Books AS B
Where B.Name LIKE '%Microsoft%' and B.Name NOT LIKE '%Windows%';

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/64.png)

___

# Task 65.

Показать все книги (название, тематика, полное имя автора в одной ячейке), цена одной страницы которых меньше 65 копеек.

Select B.Name + ' | ' + T.Name + ' | ' + A.Name + ' ' + A.Surname as [Книги]
From Books as B, Themes as T, Authors as A
where B.ThemeId = T.Id and B.AuthorId = A.Id and B.Price / B.Pages < 0.65

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/65.png)

___

# Task 66.

Показать все книги, название которых состоит из 4 слов.

Select B.Name
From Books as B
where B.Name LIKE '% % % %' and B.Name NOT LIKE '% % % % %'

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/66.png)

___

# Task 67.

Показать информацию о продажах в следующем виде:
Название книги, но, чтобы оно не содержало букву «А».
Тематика, но, чтобы не «Программирование».
Автор, но, чтобы не «Герберт Шилдт».
Цена, но, чтобы в диапазоне от 10 до 20 гривен.
Количество продаж, но не менее 8 книг.
Название магазина, который продал книгу, но он не
должен быть в Украине или России.

Select B.Id, B.Name,T.Name, A.Name, A.Surname, S.Price, S.Quantity 
From Books as B, Themes as T, Authors as A, Sales as S, Shops as M, Countries as C
where B.Name NOT LIKE '%А%' and T.Name NOT LIKE 'Программирование'
and A.Name NOT LIKE 'Герберт' and A.Surname NOT LIKE 'Шилдт' 
and S.Price >=10 and S.Price <= 20
and S.Quantity >= 8
and (C.Name NOT LIKE 'Россия' OR C.Name NOT LIKE 'Украина')
and B.Id = S.BookId and B.AuthorId = A.Id and B.ThemeId = T.Id
and M.CountryId = C.Id and M.Id = S.ShopId

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/67.png)

___

# Task 68.

Показать следующую информацию в два столбца (числа в правом столбце приведены в качестве примера):
Количество авторов: 14
Количество книг: 47
Средняя цена продажи: 85.43 гри.
Среднее количество страниц: 650.6.

Select 'Количество авторов' as N1, Count(*) as N2
From Authors
Union all
Select 'Количество книг' as N1, Count(*) as N2
From Books
Union all
Select 'Средняя цена продажи' as N1, AVG(Price) as N2
From Sales
Union all
Select 'Среднее количество страниц' as N1, AVG(Pages) as N2
From Books

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/68.png)

___

# Task 69.

Показать тематики книг и сумму страниц всех книг по каждой из них.

Select T.Name, Sum(B.Pages) as[Сумма страниц]
From Themes as T, Books as B
where B.ThemeId = T.Id 
Group by T.Name

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/69.png)

___

# Task 70.

Показать количество всех книги сумму страницэтих книг по каждому из авторов.

Select (A.Name +' '+ A.Surname) as Fullname, Sum(B.Pages) as[Сумма страниц], Count(B.Name) as[Количество книг]
From Authors as A, Books as B
where A.Id = B.AuthorId 
Group by A.Name, A.Surname

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/70.png)

___

# Task 71.

Показать книгу тематики «Программирование» с наибольшим количеством страниц.

Select B.Name, T.Name, B.Pages
From Themes as T, Books as B, 
(select Max(B.Pages) as CountPage From Themes as T, Books as B
where T.Id = B.ThemeId and T.Name LIKE 'Программирование') as G
where T.Id = B.ThemeId and T.Name LIKE 'Программирование' and G.CountPage = B.Pages

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/71.png)

___

# Task 72.

Показать среднее количество страниц по каждой тематике, которое не превышает 400.

Select T.Name
From Themes as T, Books as B, 
(Select Th.Name as Sn, AVG(Bo.Pages) as Sp 
From Themes as Th, Books as Bo 
where Th.Id = Bo.ThemeId Group by Th.Name) as D
where T.Id = B.ThemeId and D.Sp <= 400 and T.Name = D.Sn
Group by T.Name

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/72.png)

___

# Task 73.

Показать сумму страниц по каждой тематике, учитывая
только книги с количеством страниц более 400, и чтобы
тематики были «Программирование», «Администриро-вание» и «Дизайн».

Select T.Name, D.Sp as [Количество страниц]
From Themes as T, Books as B, 
(Select Th.Name as Sn, Sum(Bo.Pages) as Sp 
From Themes as Th, Books as Bo 
where Th.Id = Bo.ThemeId and Bo.Pages > 400 Group by Th.Name) as D
where T.Id = B.ThemeId and T.Name = D.Sn and (T.Name Like 'Программирование' OR T.Name Like 'Администратирование'OR T.Name Like 'Дизайн')
Group by T.Name, D.Sp

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/73.png)

___

# Task 74.

Показать информацию о работе магазинов: что, где, кем, когда и в каком количестве было продано.

Select B.Name as [Проданая книга], C.Name as [Страна], S.Name as [Название магазина], Sal.Quantity as [Количество], Sal.SaleDate as [Дата продажи]
From Shops as S, Books as B, Sales as Sal, Countries as C
where B.Id = Sal.BookId and Sal.ShopId = S.Id and C.Id = S.CountryId

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/74.png)

___

# Task 75.

Показать самый прибыльный магазин.

Select Sh.Name, R.Summa
From Shops as Sh, Sales as S,
(
Select S.ShopId as Bid, Sum(S.Price*S.Quantity) as Summa
from Sales as S, Books as B
where B.Id = S.BookId
Group by S.ShopId
)as R,
(
Select Max(Big.Summa) as BS
From 
(
Select B.Id as Bid, Sum(S.Price*S.Quantity) as Summa
from Sales as S, Books as B
where B.Id = S.BookId
Group by B.Id
) as Big
) as Q
where Sh.Id = S.ShopId and Q.BS = R.Summa and R.Bid = Sh.Id

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/75.png)

___

# Task 76.

Показать все книги жанра «Детектив», количество проданных книг более 30 экземпляров.

Select B.Name
From Books AS B
INNER JOIN  Themes AS T 
ON T.Id = B.ThemeId
INNER JOIN Sales AS S
ON S.BookId = B.Id
Where T.Name LIKE 'Детектив' AND Quantity > 30

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/76.png)

___

# Task 77.

Показать все книги (название, тематика, полное имя автора в одной ячейке), цена одной страницы которых меньше 65 копеек.

Select B.Name + ' | ' + T.Name + ' | ' + A.Name + ' ' + A.Surname as [Книги]
From Books as B
join Themes as T
on B.ThemeId = T.Id
join Authors as A
on B.AuthorId = A.Id
where B.Price / B.Pages < 0.65

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/77.png)

___

# Task 78.

Показать информацию о продажах в следующем виде:
Название книги, но, чтобы оно не содержало букву «А».
Тематика, но, чтобы не «Программирование».
Автор, но, чтобы не «Герберт Шилдт».
Цена, но, чтобы в диапазоне от 10 до 20 гривен.
Количество продаж, но не менее 8 книг.
Название магазина, который продал книгу, но он не
должен быть в Украине или России.

Select B.Id, B.Name as [Название книги],T.Name as [Жанр], A.Name + ' ' + A.Surname as [Автор],  S.Price as [Цена], S.Quantity  as [Количество]
From Books as B 
join Themes as T on B.ThemeId = T.Id
join Authors as A on B.AuthorId = A.Id
join Sales as S on B.Id = S.BookId
join Shops as M on M.Id = S.ShopId
join Countries as C on M.CountryId = C.Id 
where B.Name NOT LIKE '%А%' and T.Name NOT LIKE 'Программирование'
and A.Name NOT LIKE 'Герберт' and A.Surname NOT LIKE 'Шилдт' 
and S.Price >=10 and S.Price <= 20
and S.Quantity >= 8
and (C.Name NOT LIKE 'Россия' OR C.Name NOT LIKE 'Украина')

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/78.png)

___

# Task 79.

Показать следующую информацию в два столбца (числа в правом столбце приведены в качестве примера):
Количество авторов: 14
Количество книг: 47
Средняя цена продажи: 85.43 грн.
Среднее количество страниц: 650.6.
Количество магазинов.
Количество жанров.

Select 'Количество авторов' as N1, Count(*) as N2
From Authors
Union all
Select 'Количество книг' as N1, Count(*) as N2
From Books
Union all
Select 'Средняя цена продажи' as N1, AVG(Price) as N2
From Sales
Union all
Select 'Среднее количество страниц' as N1, AVG(Pages) as N2
From Books
Union all
Select 'Количество магазинов' as N1, Count(*) as N2
From Shops
Union all
Select 'Количество жанров' as N1, Count(*) as N2
From Themes
Union all
Select 'Количество жанров' as N1, Count(*) as N2

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/79.png)

___

# Task 80.

Показать тематики книг и сумму страниц всех книг по каждой из них.

Select T.Name, Sum(B.Pages) as[Сумма страниц]
From Themes as T join Books as B
on B.ThemeId = T.Id 
Group by T.Name

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/80.png)

___

# Task 81.

Показать количество всех книги сумму страницэтих книг по каждому из авторов.

Select (A.Name +' '+ A.Surname) as [Автор], Sum(B.Pages) as[Сумма страниц], Count(B.Name) as[Количество книг]
From Authors as A join Books as B
on A.Id = B.AuthorId 
Group by A.Name, A.Surname

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/81.png)

___

# Task 82.

Показать книгу тематики «Программирование» с наибольшим количеством страниц.

Select B.Name, T.Name, B.Pages
From Themes as T join Books as B
on T.Id = B.ThemeId , 
(select Max(B.Pages) as CountPage From Themes as T, Books as B
where T.Id = B.ThemeId and T.Name LIKE 'Программирование') as G
where T.Id = B.ThemeId and T.Name LIKE 'Программирование' and G.CountPage = B.Pages

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/82.png)

___

# Task 83.

Минимальные затраты на 1 посетителя

Select Min(TotalCosts / QuantityClients) as [Минимальные затраты на 1 посетителя]
From Market;

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/83.png)

___

# Task 84.

В какой день предприятие заработало максимальную общию прибыль

Select Date as [Дата максимальной прибыли] From Market
Where QuantityClients*Profit = (Select Max(QuantityClients * Profit)From Market);

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/84.png)

___

# Task 85.

Сумма прибыли за все вторники

Select Sum(QuantityClients*Profit) as [Сумма прибыли за все вторники]
From Market
Where Reclame LIKE 'радио';

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/85.png)

___

# Task 86.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/86.png)


use [master];
go

if db_id('Phonebook') is not null
begin
	drop database [Phonebook];
end
go

create database [Phonebook];
go

use [Phonebook];
go
create table [People]
(
	[Id] int not null identity(1, 1) primary key,
	[LastName] nvarchar(100) not null check ([LastName] <> N''),
	[FirstName] nvarchar(100) not null check ([FirstName] <> N''),
	[SurName] nvarchar(100) not null check ([SurName] <> N''),
	[Sex] nvarchar(100) not null check ([Sex] <> N''),
	[DateBirth] DateTime not null,
	[Telephone] nvarchar(13) not null check ([Telephone] <> N''),
	[Town] nvarchar(100) not null check ([Town] <> N''),
	[Country] nvarchar(100) not null check ([Country] <> N''),
	[Adress] nvarchar(100) not null check ([Adress] <> N'')
);
go

___

# Task 87.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/87.png)


use [master];
go

if db_id('Sales') is not null
begin
	drop database [Sales];
end
go

create database [Sales];
go

use [Sales];
go
create table [Sellers]
(
	[Id] int not null identity(1, 1) primary key,
	[LastName] nvarchar(100) not null check ([LastName] <> N''),
	[FirstName] nvarchar(100) not null check ([FirstName] <> N''),
	[SurName] nvarchar(100) not null check ([SurName] <> N''),
	[Telephone] nvarchar(13) not null check ([Telephone] <> N''),
	[Email] nvarchar(100) not null check ([Email] <> N'')
);
go
create table [Buyers]
(
	[Id] int not null identity(1, 1) primary key,
	[LastName] nvarchar(100) not null check ([LastName] <> N''),
	[FirstName] nvarchar(100) not null check ([FirstName] <> N''),
	[SurName] nvarchar(100) not null check ([SurName] <> N''),
	[Telephone] nvarchar(13) not null check ([Telephone] <> N''),
	[Email] nvarchar(100) not null check ([Email] <> N'')
);
go
create table [Sales]
(
	[BuyersId] int not null,
	[SellersId] int not null,
	[NameProduct] nvarchar(100) not null check ([LastName] <> N''),
	[Price] money not null,
	[Date] date not null
);
go

___

# Task 88.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/88.png)


use [master];
go

if db_id('MusicCollection') is not null
begin
	drop database [MusicCollection];
end
go

create database [MusicCollection];
go

use [MusicCollection];
go

create table [Disk]
(
	[Id] int not null identity(1, 1) primary key,
	[Название] nvarchar(100) not null,
	[Исполнитель] nvarchar(100) not null,
	[ДатаВыпуска] date not null,
	[Стиль] nvarchar(50) not null,
	[Издатель] nvarchar(50) not null,
);
go
create table [Styles]
(
	[Id] int not null identity(1, 1) primary key,
	[Название] nvarchar(100) not null,
);
go
create table [Singer]
(
	[Id] int not null identity(1, 1) primary key,
	[Название] nvarchar(100) not null,
);
go
create table [Country]
(
	[Id] int not null identity(1, 1) primary key,
	[Страна] nvarchar(50) not null,
);
go
create table [Songs]
	(
	[НазваниеПесни] nvarchar(50) not null,
	[НазваниеДиска] nvarchar(50) not null,
	[Длительность] nvarchar(50) not null,
	[Стиль] nvarchar(50) not null,
	[Исполнитель] nvarchar(50) not null,
	);

___