<!-- Contare quanti studenti ci sono stati ogni anno -->

SELECT COUNT(\*) AS `numero_studenti`, YEAR (`enrolment_date`) AS `anno_di_immatricolazione`
FROM `students`
GROUP BY `anno_di_immatricolazione`
ORDER BY `anno_di_immatricolazione` DESC

<!-- Contare gli insenganti che hanno l'uffico nello stesso edificio -->

SELECT COUNT(\*) AS `numero_insegnanti`, `office_address` AS `indirizzo_ufficio`
FROM `teachers`
GROUP BY `indirizzo_ufficio`
