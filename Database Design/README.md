# Description
---
The database is a school design database where student and school information and relations are displayed. The design shows student information regarding their courses and schools they attend and their grade levels relative to the courses they are taking.

# Tables
---
### student
- studentID int primary key
- firstName varchar(25)
- lastName varchar(50)
- gradeLevel int
### school
- schoolID int primary key
- schoolName varchar(30)
- schoolAddress varchar(30)
### course
- courseID int primary key
- courseName varchar(25)
- courseSection int
### studentCourse
- studentID int foreign key references student(studentID)
- courseID int foreign key references course(courseID)
- courseGrade int
### schoolCourse
- schoolID int foreign key references school(schoolID)
- courseID int foreign key references course(courseID)
### studentAttendSchool
- studentID int foreign key references student(studentID)
- schoolID int foreign key references school(schoolID)
