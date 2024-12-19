<!-- Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia -->

SELECT \*
FROM `students`
LEFT JOIN `degrees`
ON`degrees`.`name`= "Corso di Laurea in Economia"

<!-- Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze -->

SELECT \*
FROM `degrees`
LEFT JOIN `departments`
ON `departments`.`id` = `degrees`.`department_id`
WHERE `degrees`.`level`= "magistrale"

<!-- Selezionare tutti i corsi in cui insegna il docente con ID=44 -->

SELECT \*
FROM `courses`
LEFT JOIN `teachers`
ON `teachers`.`id` = 44

<!-- Selezionare tutti gli studenti-corsi-dipartimenti in ordine alfabetico per cognome -->

SELECT \*
FROM `students`
LEFT JOIN `degrees`
ON `degrees`.`id` = `students`.`degree_id`
LEFT JOIN `departments`
ON `departments`.`id` = `degrees`.`department_id`
ORDER BY `students`.`surname`ASC
