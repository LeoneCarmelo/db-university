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