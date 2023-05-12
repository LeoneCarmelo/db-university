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
