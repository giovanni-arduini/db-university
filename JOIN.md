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
