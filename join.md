# Query Todo

## 1) Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia
```sql

SELECT * 
FROM `degrees`
JOIN `students`
ON `students`.`degree_id` = `degrees`.`id`
WHERE `degrees`.`name` = 'Corso di Laurea in Economia'

```

## 2) Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze
```sql

SELECT * 
FROM `degrees`
JOIN `departments`
ON `department_id` = `degrees` . `department_id`
WHERE `departments`.`name` = 'Dipartimento di Neuroscienze'

```

## 5) Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti
```sql

FROM `degrees`
JOIN `courses`
ON `degree_id` = `degrees` . `id`
JOIN `course_teacher`
ON `courses` . `id` = `course_id`
JOIN `teachers`
ON `teacher_id` = `teachers` . `id`

```