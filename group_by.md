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