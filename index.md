# Graph Database Exercises

# Exercise 1
## Example DB
* connect 192.168.182.201:2480
* login into db "demo"
    * user : root
    * pass : password

## Schema
* Teacher ==Teach=> Subject
* Teacher ==Teaching=> Classroom
* Student ==Attend=> Subject (Register)
* Student ==Attending=> Classroom

## Problems
* Select all student's name
* Select all teacher's name
* Select all subject's name
* Select all subject's name along with number of student attended to this subject
* Select all teacher's name along with their subjects
* Select all class along with teacher who is teaching in this class
* Select all student's name along with subject they've attended
* Select all student's name along with subject they've attended and name of teachers who's teaching these subjects
* Select all student's name along with class they're attending
* Select all student's name along with class they're attending and teacher who's teaching in that class along with their subjects

## Exercise 2
### Schema
```sql
create class person if not exists extends V
create property person.name STRING
create property person.age INTEGER

create class student if not exists extends person
create property student.year INTEGER

create class subject if not exists extends V
create property subject.name STRING

create class classroom if not exists extends V
create property classroom.name STRING

create class subject_classroom if not exists extends E
create property subject_classroom.date STRING
create property subject_classroom.timestart INTEGER
create property subject_classroom.timeend INTEGER

create class student_subject if not exists extends E
create property student_subject.score INTEGER
```

### Problems
* add 8 students into db
    * name "A" year 1
    * name "B" year 1
    * name "C" year 1
    * name "D" year 2
    * name "E" year 2
    * name "F" year 3
    * name "G" year 3
    * name "H" year 4
* add 4 subjects into do
    * name "Math"
    * name "Physics"
    * name "English"
    * name "Biology"
* add 3 classrooms into db
    * name "C-101"
    * name "C-102"
    * name "C-103"

* set class Math to classroom "C-101" at Monday 540(09.00)-720(12.00) and Friday 540-720
* set class Math to classroom "C-102" at Monday 780-960 and Tuesday 780-960
* set class Math to classroom "C-103" at Wednesday 780-960 and Friday 780-960

* set class Physics to classroom "C-101" at Tuesday 540-720
* set class Physics to classroom "C-102" at Monday 540-720, Wednesday 540-720 and Friday 780-960
* set class Physics to classroom "C-103" at Thursday 540-720 and Friday 540-720

* set class English to classroom "C-101" at Monday 780-960 and Wednesday 780-960
* set class English to classroom "C-102" at Tuesday 540-720
* set class English to classroom "C-103" at Monday 540-720, Wednesday 540-720 and Thursday 780-960

* set class Biology to classroom "C-101" at Tuesday 780-960, Wednesday 540-720 and Friday 780-960
* set class Biology to classroom "C-102" at Wednesday 780-960, Thursday 540-720 and Friday 540-720
* set class Biology to classroom "C-103" at Monday 780-960, Tuesday 540-720and Thursday 780-960
