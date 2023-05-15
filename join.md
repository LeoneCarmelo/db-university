# query 1
SELECT * 
FROM `students` 
JOIN `degrees` ON `degree_id` = `degrees`.`id` 
WHERE `degrees`.`name` = 'Corso di Laurea in Economia'; 