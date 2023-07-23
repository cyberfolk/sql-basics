# GROUP BY

## Contare quanti iscritti ci sono stati ogni anno

> SELECT YEAR(`enrolment_date`) AS `year`, COUNT(\*) AS `enrolment_numeber`  
> FROM `students`  
> GROUP BY YEAR(`enrolment_date`)

## Contare gli insegnanti che hanno l'ufficio nello stesso edificio

> SELECT `office_address` AS `address`, COUNT(\*) AS `shared_number`  
> FROM `teachers`  
> GROUP BY `office_address`

## Calcolare la media dei voti di ogni appello d'esame

> SELECT `exam_id`, AVG(`vote`) AS `vote_avg`
> FROM `exam_student`  
> GROUP BY `exam_id`

## Contare quanti corsi di laurea ci sono per ogni dipartimento

> SELECT `departments`.`name` AS `department_name`, COUNT(`degrees`.`id`) AS `degree_number`  
> FROM `departments`  
> JOIN `degrees` ON `departments`.`id` = `degrees`.`department_id`  
> GROUP BY `departments`.`id`
