1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia

    SELECT * FROM `students` LEFT JOIN `degrees` ON `students`.`degree_id` = `degrees`.`id` WHERE `degrees`.`name` = 'corso di laurea in economia'

2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze

    SELECT * FROM `degrees` JOIN `departments` ON `degrees`.`department_id` = `departments`.`id` WHERE `degrees`.`level` = "magistrale" AND `departments`.`name` = "dipartimento di neuroscienze"

3.  Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)

    SELECT * FROM `teachers` JOIN `course_teacher` ON `teachers`.`id` = `course_teacher`.`course_id` JOIN `courses` ON `course_teacher`.`course_id` = `courses`.`id` WHERE `teachers`.`id` = 44

4.  Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome

    SELECT * FROM `students` JOIN `courses` ON `students`.`degree_id` = `courses`.`id` JOIN `departments` ON `courses`.`id` = `departments`.`id` ORDER BY `students`.`name` ASC

5.  