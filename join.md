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

# query 4
SELECT
 `students`.`surname` AS `student_surname`,
 `students`.`name` AS `student_name`,
 `degrees`.`name` AS `degree_name`,
 `degrees`.`level` AS `degree_level`,
 `degrees`.`address` AS `degree_address`,
 `degrees`.`email` AS `degree_email`,
 `degrees`.`website` AS `degree_website`,
 `departments`.`name` as `department_name`
FROM
    `students`
JOIN `degrees` ON students.degree_id = `degrees`.`id`
JOIN `departments` ON DEGREES.department_id = `departments`.`id`
ORDER BY `student_surname`;

# query 5
SELECT
 `degrees`.`name` AS `degree_name`,
 `courses`.`name` AS `course_name`,
 `teachers`.`name` AS `teacher_name`,
 `teachers`.`surname` AS `teacher_surname`

FROM
    `course_teacher`
JOIN `teachers` ON course_teacher.teacher_id = `teachers`.`id`
JOIN `courses` ON course_teacher.course_id = `courses`.`id`
JOIN `degrees` ON `courses`.`degree_id` = `degrees`.`id`;

# query 6
SELECT
 `teachers`.`name` AS `teacher_name`,
 `teachers`.`surname` AS `teacher_surname`,
 `departments`.`name` AS `departments_name`

FROM
    `course_teacher`
JOIN `teachers` ON course_teacher.teacher_id = `teachers`.`id`
JOIN `courses` ON course_teacher.course_id = `courses`.`id`
JOIN `degrees` ON `courses`.`degree_id` = `degrees`.`id`
JOIN `departments` ON `degrees`.`department_id` = `departments`.`id`
WHERE `departments`.`name` = 'Dipartimento di Matematica';