**Esercizio n.1**
- SELECT COUNT(*) as `num_students`, YEAR(`enrolment_date`) as `student_every_year`
FROM `students`
GROUP BY `student_every_year`;

**Esercizio n.2**
- SELECT COUNT(*) as `num_teachers`, `office_address` as `every_office`
FROM `teachers`
GROUP BY `every_office`;

**Esercizio n.3**
- SELECT `exam_id`, AVG(`vote`) as `avg_vote`
FROM `exam_student`
GROUP BY `exam_id`;

**Esercizio n.4**
- SELECT `department_id`, COUNT(*) AS `num_courses`
FROM `degrees`
GROUP BY `department_id`;