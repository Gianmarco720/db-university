# Query Todo

## 1) Contare quanti iscritti ci sono stati ogni anno
```sql

SELECT COUNT(`id`) AS `enrolled_students_number`
FROM `students`
GROUP BY YEAR(`enrolment_date`);

```

## 2) Contare gli insegnanti che hanno l'ufficio nello stesso edificio
```sql

SELECT COUNT(`id`) AS `same_bubilding_office`
FROM `teachers`
GROUP BY `office_address`;

```

## 3) Calcolare la media dei voti di ogni appello d'esame
```sql

SELECT AVG(`vote`) AS `grade_point_average`
FROM `exam_student`
GROUP BY `student_id`;

```

## 4) Contare quanti corsi di laurea ci sono per ogni dipartimento
```sql

SELECT COUNT(`id`) AS `total_departments_per_degree`
FROM `degrees`
GROUP BY `department_id`;

```