# query 1
SELECT
    students.*
FROM
    students
JOIN DEGREES ON students.degree_id = DEGREES.id
WHERE
    DEGREES.name = 'Corso di Laurea in Economia';

# query 2
SELECT
    `degrees`.*
FROM
    `degrees`
JOIN `departments` ON DEGREES.department_id = `departments`.`id`
WHERE
    departments.name = 'Dipartimento di Neuroscienze' AND `degrees`.`name` LIKE 'Corso di Laurea Magistrale%';

# query 3
SELECT
    `courses`.`name` AS `course_name`,
    `teachers`.`id`,
    `teachers`.`name`,
    `teachers`.`surname`,
    `teachers`.`email`
FROM
    `course_teacher`
JOIN `teachers` ON course_teacher.teacher_id = `teachers`.`id`
JOIN `courses` ON course_teacher.course_id = `courses`.`id`
WHERE
    teachers.id = 44;