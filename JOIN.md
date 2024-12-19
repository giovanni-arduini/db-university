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
