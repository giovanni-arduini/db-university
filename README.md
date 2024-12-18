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

<!-- selezionare esami dopo le 14:00 il giorno 20/06/2020 -->

SELECT \* FROM `exams`
WHERE `date` = "2020/06/20"
AND `hour` >= "14:00:00"

<!-- selezionare tutti i corsi di laurea magistrale -->

SELECT \* FROM `degrees`
WHERE `level` = "magistrale"

<!-- da quanti dipartimenti è composta l'università? -->

SELECT COUNT(\*) AS `numero_dipartimenti` FROM `departments`

<!-- Quanti sono gli insegnanti senza numero di telefono? -->

SELECT COUNT(\*) AS `insegnanti_senza_numero_telefonico`
FROM `teachers`
WHERE `phone` IS NULL

<!-- Inserire nella tabella studenti un nuovo record con i propri dati -->

INSERT INTO `university`.`students` (`id`, `degree_id`, `name`, `surname`, `date_of_birth`, `fiscal_code`, `enrolment_date`, `registration_number`, `email`) VALUES ('69696', '3', 'Giovanni', 'Arduini', '1991-04-20', 'RDNGNN91D20F205V', '2010-08-29', '743099', 'g.arduini@lollo.com');

<!-- cambiare il numero di ufficio del prof. Pietro Rizzo in 126 -->

UPDATE `university`.`teachers` SET `office_number` = '126' WHERE (`id` = '58');

<!-- eliminare dalla tabella studenti il proprio record -->

DELETE FROM `university`.`students` WHERE (`id` = '5001');
