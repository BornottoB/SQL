# SQL
SQL
Ниже приведена структура базы данных, в которой отражена зависимость между
списком стажёров (таблица “Trainee”) и курсами (таблица “Course”), которые они
проходили. Из таблицы “History” можно получить информацию о том, какой стажёр
проходил выбранный курс, сколько это заняло времени (поля “from” и “to”) и был ли
выбранный курс засчитан (поле “status”).
Trainee
trainee_id int(10) unsigned Primary key: unique trainee ID.
name varchar(255) Name of trainee.
email varchar(255) Email of trainee.
Course
course_id int(10) unsigned Primary key: unique course ID.
name varchar(255) Name of course.
description varchar(255) Description of course.
History
history_id int(10) unsigned Primary key: unique history ID.
trainee_id int(10) unsigned Trainee ID.
course_id int(10) unsigned Course ID.
start int(11) Timestamp for when course was started.
end int(11) Timestamp for when course was finished.
status tinyint(4) Whether the course was passed(1) or not(0).
1. создайте базу данных “Training”;
2. создайте указанные выше таблицы;
3. заполните их данными таким образом, чтобы информации было достаточно для
выполнения требуемых запросов (т.е. они бы возвращали непустой результат);
4. выведите список стажёров (trainee name, trainee email, course name, history end)
которые успешно прошли курс PHP (course name=PHP) в прошлом месяце
(сравнить history end);
5. для каждого из всех возможных курсов выведите количество успешных
прохождений (course name, quantity) в текущем месяце (сравнить history start);
