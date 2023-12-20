**Esercizio n.1**
- SELECT *
FROM `students`
WHERE `date_of_birth` like '1990-%'
ORDER BY `date_of_birth` ASC;

**Esercizio n.2**
- SELECT *
FROM `courses`
WHERE `cfu` > '10'
ORDER BY `cfu` ASC;

**Esercizio n.3**
- SELECT *
FROM `students`
WHERE DATEDIFF (CURRENT_DATE, `date_of_birth`) / 365 > 30
ORDER BY `date_of_birth` DESC;

**Esercizio n.4**
- SELECT *
FROM `courses`
WHERE `period` = 'I semestre'
AND `year` = '1';

**Esercizio n.5** (da rivedere)
- SELECT *
FROM `exams`
WHERE `date` = '2020/06/20'
AND `hour` > '16:%'
ORDER BY `hour` ASC;

**Esercizio n.6**
- SELECT *
FROM `degrees`
WHERE `level` = 'magistrale'
ORDER BY `name` ASC;

**Esercizio n.7**
- SELECT COUNT(*)
FROM `departments`;

**Esercizio n.8**
- SELECT COUNT(*)
FROM `teachers`
WHERE `phone` is NULL;