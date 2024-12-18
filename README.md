<!-- selezionare tutti gli studenti nati nel 1990 -->

SELECT \* FROM `students`
WHERE `date_of_birth` LIKE "1990-%"

<!-- selezionare tutti i corsi da più di 10 cfu -->

SELECT \* FROM `courses`
WHERE `cfu` > 10

<!-- selezionare tutti i corsi del primo semestre del primo anno  -->

SELECT \* FROM `courses`
WHERE `year` = 1
AND `period` LIKE "I semestre"
