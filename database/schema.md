# ClassConnect Database Schema

## Tables

### Users
- id (Primary Key)
- name
- email
- role (student, lecturer, admin)
- password_hash
- created_at

### Courses
- id (Primary Key)
- name
- code
- lecturer_id (Foreign Key)
- semester

### Attendance
- id (Primary Key)
- student_id (Foreign Key)
- course_id (Foreign Key)
- date
- present (true/false)

### Grades
- id (Primary Key)
- student_id (Foreign Key)
- course_id (Foreign Key)
- assessment_type (quiz, assignment, exam)
- score
- date_recorded

### AcademicStanding
- id (Primary Key)
- student_id (Foreign Key)
- gpa
- status (good_standing, probation, at_risk)