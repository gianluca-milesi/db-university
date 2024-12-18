### Selezionare tutti gli studenti nati nel 1990 (160)
```
SELECT * FROM `students` WHERE `date_of_birth` LIKE '1990-%';
```

### Selezionare tutti i corsi che valgono più di 10 crediti (479)
```
SELECT * FROM `courses` WHERE `cfu` > 10;
```

### Selezionare tutti gli studenti che hanno più di 30 anni
```
SELECT * FROM `students` WHERE `date_of_birth` <= '1994-12-31';
```

### Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di laurea (286)
```
SELECT * FROM `courses` WHERE `period` = 'I semestre' AND `year` = '1';
```

### Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del 20/06/2020 (21)
```
SELECT * FROM `exams` WHERE `date` = '2020-06-20' AND `hour` > '14:00:00';
```

### Selezionare tutti i corsi di laurea magistrale (38)
```
SELECT * FROM `degrees` WHERE `level` = 'magistrale';
```

### Da quanti dipartimenti è composta l'università? (12)
```
SELECT * FROM `db_university`.`departments`;
```

### Quanti sono gli insegnanti che non hanno un numero di telefono? (50)
```
SELECT * FROM `teachers` WHERE `phone` IS NULL;
```

### Inserire nella tabella degli studenti un nuovo record con i propri dati (per il campo degree_id, inserire un valore casuale)
```
INSERT INTO `students` (degree_id, name, surname, date_of_birth, fiscal_code, enrolment_date, registration_number, email)
VALUES (1, 'Gianluca', 'Milesi', '1999-04-15', 'MLSGLC99DH501U', '2024-12-18', 620040, 'gianluca.milesi.99@gmail.com');
```

### Cambiare il numero dell’ufficio del professor Pietro Rizzo in 126
```
UPDATE `teachers`
SET `office_number` = 126
WHERE `id` = 58;
```

### Eliminare dalla tabella studenti il record creato precedentemente al punto 9
```
DELETE FROM `students`
WHERE `id` = 5001;

oppure con i valori

DELETE FROM `students`
WHERE `id` = 5001 AND `degree_id` = 1 `name` = 'Gianluca' AND `surname` = 'Milesi' AND `date_of_birth` = '1999-04-15' AND `fiscal_code` = 'MLSGLC99DH501U' AND `enrolment_date` = '2024-12-18' AND `registration_number` = 620040 AND `email` = 'gianluca.milesi.99@gmail.com';
```