**Esercizio n.1**
- SELECT * 
FROM `students`
INNER JOIN `degrees`
ON `students`.`degree_id` = `degrees`.`id`
WHERE `degrees`.`name` = "Corso di Laurea in Economia";

**Esercizio n.2**
- SELECT * 
FROM `degrees`
INNER JOIN `departments`
ON `degrees`.`department_id` = `departments`.`id`
WHERE `departments`.`name` = "Dipartimento di Neuroscienze"
AND `degrees`.`level` = "magistrale";

**Esercizio n.3**
- SELECT * 
FROM `courses`
INNER JOIN `teachers`
ON `courses`.`id` = `teachers`.`id`
WHERE `teachers`.`id` = "44";

**Esercizio n.4**
- SELECT * 
FROM `students`
INNER JOIN `degrees`
ON `students`.`degree_id` = `degrees`.`id`
INNER JOIN `departments`
ON `degrees`.`department_id` = `departments`.`id`
ORDER BY `students`.`surname`, `students`.`name` ASC;

**Esercizio n.5**
- SELECT * 
FROM `degrees`
INNER JOIN `courses`
ON `courses`.`degree_id` = `degrees`.`id`
INNER JOIN `teachers`
ON `courses`.`id` = `teachers`.`id`
ORDER BY `degrees`.`name`, `courses`.`year`, `courses`.`period` ASC;

**Esercizio n.6**
- SELECT `teachers`.`name`, `teachers`.`surname`, `departments`.`name`, `departments`.`address`
FROM `teachers`
INNER JOIN `course_teacher`
ON `teachers`.`id` = `course_teacher`.`teacher_id`
INNER JOIN `courses`
ON `course_teacher`.`course_id` = `courses`.`id`
INNER JOIN `degrees`
ON `courses`.`degree_id` = `degrees`.`id`
INNER JOIN `departments`
ON `degrees`.`department_id` = `departments`.`id`
WHERE `departments`.`name` = "Dipartimento di Matematica"
ORDER BY `teachers`.`id`;