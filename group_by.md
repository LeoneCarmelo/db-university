# query 1
SELECT
    COUNT(id),
    YEAR(`students`.`enrolment_date`)
FROM
    `students`
GROUP BY
    YEAR(`students`.`enrolment_date`);