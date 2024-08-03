Approach:

 1. Identify the entities
  -user
  -course
  -admission
  -codekata
  -mentor
  -studentsattendance
  -task
  -leaderboard


2. Identify the attributes

   -user: userid, username, useremail, usermobile
   -course: course_id, course_name, course_duration, course_fees
   -admission: userid, course_id, admission_fees
   -codekata: userid
   -mentor: userid, course_id, mentor_name
   -studentsattendance: A_id, userid, A_date, status
   -task: userid, submittedtask, task_mark
   -leaderboard: userid, course_id, batch, submitted_task

   3. Identify the primary keys
    -userid
    -course_id

   4. Identity the foregin keys
     
    -userid
    -course-id

   5. Create the table

```sql
      create table user(
userid int ,
username varchar(25),
usermobile int (10) 
);

      create table course(
course_id int ,
userid int,
course_name varchar(25),
course_duration varchar(255),
course_fees int,
);

      create table admissions(
userid int,
course_id int,
admission_fees int,
);

    create table codekata(
userid int,
solved_problem varchar(25) ,
);

    create table mentor(
userid int,
course_id int ,
mentor_name varchar(25) ,
);

      create table studentsAttendance(
A_id int,
userid int,
A_date datetime default now(),
status boolean default true,
);

      create table task(
userid int,
submited_task varchar(25) ,
task_mark int ,
);

     create table leaderboard(
userid int,
course_id int,
batch varchar(25),
submited_task varchar(25) ,
);

```

```sql
insert into user values
(1, 'A', 1234)
(2, 'B', 2344)
(3, 'C', 3445)
```

```sql
insert into course values
(4, 1, 'FSD', 'Three months', 20000)
(5, 2, 'AI', 'Two months', 25000)
(6, 3, 'Developer' 'Three months', 30000)
```

```sql
insert into admissions values
(1, 4, 500)
(2, 5, 400)
(3, 6, 600)
```

```sql
insert into codekata values
(1, 'yes')
(2, 'no')
(3, 'yes')
```

```sql
insert into mentor values
(1, 4, 'E')
(2, 5, 'F')
(3, 6, 'G')
```

```sql
insert into studentsAttendance values
(9, 1, 10/02/2024)
(8, 2, 12/03/2024)
(7, 3, 30/04/2024)
```

```sql
insert into task values
(1, 'task1', 10)
(2, 'task2', 9)
(3, 'task3', 8)
```

```sql
insert into leaderboard values
(1, 4, 56, 'yes')
(2, 5, 56, 'no')
(3, 6, 56, 'yes')
```