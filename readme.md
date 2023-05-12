## Queries
# 1
- show databases;
- use university;
- show tables;
- describe students;
- select *
  from students 
  where date_of_birth
  like '1990-%';

# 2
- show databases;
- use university;
- show tables;
- describe courses;
- select *
  from courses
  where cfu > 10;

# 3
- show databases;
- use university;
- show tables;
- describe students;
- select *
  from students
  where year(date_of_birth) < 1993
  (3501)

# 4 
- show databases;
- use university;
- show tables;
- describe courses;
- select *
  from courses
  where year = '1' and period = 'I semestre';  


  # 5
  - show databases;
  - use university;
  - show tables;
  - describe exams;
  - select *
    from exams
    where date = '2020-06-20' and hour(hour) >= 14;


# 6
  - show databases;
  - use university;
  - show tables;
  - describe degrees;
  - select *
    from degrees
    where name like 'Corso di Laurea Magistrale%';