# JOIN

## Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia

> SELECT `students`.`name` AS `student_name`, `students`.`surname` AS `student_surname`  
> FROM `students`  
> JOIN `degrees` ON `students`.`degree_id` = `degrees`.`id`  
> WHERE `degrees`.`name`= 'Corso di Laurea in Economia';

## Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze

> SELECT `degrees`.`name` AS 'degree_name'  
> FROM `degrees`  
> JOIN `departments` ON `degrees`.`department_id` = `departments`.`id`  
> WHERE `departments`.`name` = 'Dipartimento di Neuroscienze'  
> AND `degrees`.`level` = 'magistrale';

## Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)

> SELECT `courses`.`name` AS 'cours_name'  
> FROM `course_teacher`  
> JOIN `courses`ON `course_teacher`.`course_id` = `courses`.`id`  
> JOIN `teachers`ON `course_teacher`.`teacher_id` = `teachers`.`id`  
> WHERE `teachers`.`id` = 44

## Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome

> Select `students`.`surname` AS `students_surname`, `students`.`name` AS `student_name`, `degrees`.`name` AS `degree_name`, `departments`.`name` AS `departement_name`  
> FROM `students`  
> JOIN `degrees`ON `students`.`degree_id`=`degrees`.`id`  
> JOIN `departments` ON `degrees`.`department_id`=`departments`.`id`  
> ORDER BY `students`.`surname` ASC, `students`.`name` ASC

## Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti

> .  
> .  
> .

## Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)

> .  
> .  
> .

## BONUS: Selezionare per ogni studente quanti tentativi d’esame ha sostenuto per superare ciascuno dei suoi esami

> .  
> .  
> .
