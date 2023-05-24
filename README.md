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

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/26.png)

___

# Task 27.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/27.png)

___

# Task 28.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/28.png)

___

# Task 29.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/29.png)

___

# Task 30.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/30.png)

___

# Task 31.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/31.png)

___

# Task 32.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/32.png)

___

# Task 33.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/33.png)

___

# Task 34.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/34.png)

___

# Task 35.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/35.png)

___

# Task 36.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/36.png)

___

# Task 37.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/37.png)

___

# Task 38.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/38.png)

___

# Task 39.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/39.png)

___

# Task 40.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/40.png)

___

# Task 41.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/41.png)

___

# Task 42.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/42.png)

___

# Task 43.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/43.png)

___

# Task 44.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/44.png)

___

# Task 45.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/45.png)

___

# Task 46.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/46.png)

___

# Task 47.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/47.png)

___

# Task 48.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/48.png)

___

# Task 49.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/49.png)

___

# Task 50.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/50.png)

___

# Task 51.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/51.png)

___

# Task 52.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/52.png)

___

# Task 53.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/53.png)

___

# Task 54.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/54.png)

___

# Task 55.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/55.png)

___

# Task 56.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/56.png)

___

# Task 57.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/57.png)

___

# Task 58.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/58.png)

___

# Task 59.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/59.png)

___

# Task 60.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/60.png)

___

# Task 61.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/61.png)

___

# Task 62.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/62.png)

___

# Task 63.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/63.png)

___

# Task 64.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/64.png)

___

# Task 65.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/65.png)

___

# Task 66.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/66.png)

___

# Task 67.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/67.png)

___

# Task 68.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/68.png)

___

# Task 69.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/69.png)

___

# Task 70.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/70.png)

___

# Task 71.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/71.png)

___

# Task 72.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/72.png)

___

# Task 73.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/73.png)

___

# Task 74.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/74.png)

___

# Task 75.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/75.png)

___

# Task 76.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/76.png)

___

# Task 77.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/77.png)

___

# Task 78.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/78.png)

___

# Task 79.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/79.png)

___

# Task 80.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/80.png)

___

# Task 81.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/81.png)

___

# Task 82.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/82.png)

___

# Task 83.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/83.png)

___

# Task 84.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/84.png)

___

# Task 85.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/85.png)

___

# Task 86.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/86.png)

___

# Task 87.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/87.png)

___

# Task 88.

![Image text](https://raw.githubusercontent.com/VLola/sql/master/images/88.png)

___