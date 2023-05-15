# query 1
SELECT
    COUNT(id),
    YEAR(`students`.`enrolment_date`)
FROM
    `students`
GROUP BY
    YEAR(`students`.`enrolment_date`);

# query 2
SELECT
    COUNT(id),
    `teachers`.`office_address`
FROM
    `teachers`
GROUP BY
    `teachers`.`office_address`;

# query 3
SELECT
    AVG(`exam_student`.`vote`) AS `average_vote`,
    `courses`.`name` AS `courses_name`,
    `degrees`.`name` AS `degree_name`
FROM
    `exam_student`
JOIN `exams` ON `exam_student`.`exam_id` = `exams`.`id`
JOIN `courses` ON `exams`.`course_id` = `courses`.`id`
JOIN `degrees` ON `courses`.`degree_id` = `degrees`.`id`
GROUP BY
    `courses`.`id`;