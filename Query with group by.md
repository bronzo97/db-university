1. Contare quanti iscritti ci sono ogni anno
    
    SELECT COUNT(ID), YEAR(`enrolment_date`) AS YEAR FROM `students` GROUP BY YEAR

2.  Contare gli insegnanti che hanno l'ufficio nello stesso edificio

    SELECT COUNT(id), `office_number` FROM `teachers` GROUP BY `office_number`

3.  Calcolare la media dei voti di ogni appello d'esame

    SELECT `exam_id`, AVG(`vote`) AS `AVERAGE` FROM `exam_student` GROUP BY `exam_id`

4.  Contare quanti corsi di laurea ci sono per ogni dipartimento

    SELECT SUM(`department_id`), `name` as `Courses` FROM `degrees` GROUP BY `name`;