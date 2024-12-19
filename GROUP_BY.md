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

```

### Contare quanti corsi di laurea ci sono per ogni dipartimento
```

```