<!-- Selezionare tutti gli studenti iscritti al corso di laurea in economia -->

SELECT \*
FROM `students`
LEFT JOIN `degrees`
ON`degrees`.`name`= "Corso di Laurea in Economia"
