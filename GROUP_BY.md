### Contare quanti iscritti ci sono stati ogni anno
```
SELECT COUNT(*) AS `total_students`, `enrolment_date` AS `year`
FROM `students`
GROUP BY `enrolment_date`;
```

### Contare gli insegnanti che hanno l'ufficio nello stesso edificio
```
SELECT COUNT(*) AS `teachers_per_office`, `office_address` AS `office` 
FROM `teachers`
GROUP BY `office_address`;
```

### Calcolare la media dei voti di ogni appello d'esame
```
SELECT `exam_id`, AVG(`vote`) AS `average_vote`
FROM `exam_student`
GROUP BY `exam_id`;
```

### Contare quanti corsi di laurea ci sono per ogni dipartimento
```
SELECT COUNT(`degrees`.`department_id`) AS `total_degrees`, `departments`.`name` AS `department_name`
FROM `degrees`
JOIN `departments` 
ON `departments`.`id` = `degrees`.`department_id`
GROUP BY `departments`.`name`;
```