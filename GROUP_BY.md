<!-- Contare quanti studenti ci sono stati ogni anno -->

SELECT COUNT(\*) AS `numero_studenti`, YEAR (`enrolment_date`) AS `anno_di_immatricolazione`
FROM `students`
GROUP BY `anno_di_immatricolazione`
ORDER BY `anno_di_immatricolazione` DESC
