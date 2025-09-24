# Campus Course & Records Manager (CCRM)

## Project Overview

The **Campus Course & Records Manager (CCRM)** is a **console-based Java
SE application** that helps institutes manage **students, courses,
enrollments, grades, and transcripts**.\
It demonstrates key **Object-Oriented Programming (OOP) principles**,
robust **exception handling**, advanced **Java I/O (NIO.2)**, **Streams
API**, **Date/Time API**, and incorporates design patterns like
**Singleton** and **Builder**.

This project is part of the **Programming in Java (CSE2006)** course.

------------------------------------------------------------------------

## Features

-   **Student Management** → Add, update, list, deactivate students;
    view profile & transcript.\
-   **Course Management** → Add, update, assign instructors, search &
    filter courses.\
-   **Enrollment & Grading** → Enroll/unenroll students, record marks,
    compute GPA, generate transcripts.\
-   **File Operations** → Import/export students & courses (CSV), backup
    data into timestamped folders, recursive file utilities.\
-   **CLI Workflow** → Menu-driven console navigation for all
    operations.

------------------------------------------------------------------------

## Tech Highlights

-   **Java SE 17+**\
-   **OOP Pillars**: Encapsulation, Inheritance, Abstraction,
    Polymorphism\
-   **Java NIO.2** for file I/O (Path, Files, backup utilities)\
-   **Streams & Lambdas** for filtering and sorting\
-   **Date/Time API** for student records and backup timestamps\
-   **Enums** for Semester and Grade\
-   **Design Patterns**: Singleton (AppConfig), Builder
    (Course/Transcript)\
-   **Exception Handling**: Checked, unchecked, and custom exceptions

------------------------------------------------------------------------

## Setup & Run

### 1. Requirements

-   JDK **17 or above**\
-   IDE: Eclipse / IntelliJ IDEA (or run from terminal)

### 2. Clone Repo

``` bash
git clone <your-repo-link>
cd CampusCourseRecordsManager
```

### 3. Compile & Run

``` bash
javac -d bin src/edu/ccrm/cli/Main.java
java -cp bin edu.ccrm.cli.Main
```

------------------------------------------------------------------------

## Usage Flow

When the program starts, you'll see a **menu-driven CLI** with options
like: 1. Manage Students\
2. Manage Courses\
3. Enrollments & Grades\
4. Import/Export Data\
5. Backup & Recursive Utilities\
6. Reports (Top Students, GPA Distribution)\
7. Exit

Example transcript generation:

``` text
Student: Arti Sharma
Reg No: 23BCE10922
Course: CSE2006 - Programming in Java
Grade: A
GPA: 8.7
```

------------------------------------------------------------------------

## Project Structure

    edu.ccrm
     ├─ cli/        → Menu & user interaction
     ├─ domain/     → Student, Instructor, Course, Enrollment, Grade, Semester
     ├─ service/    → StudentService, CourseService, TranscriptService
     ├─ io/         → Import/Export, Backup utilities
     ├─ util/       → Validators, Comparators, Recursive file utils
     └─ config/     → Singleton AppConfig, Builders

------------------------------------------------------------------------

## 📖 Theory Components

### Evolution of Java

-   1995 -- Java 1.0 released by Sun Microsystems\
-   2006 -- Java becomes open source (OpenJDK)\
-   2014 -- Java 8 introduces Streams & Lambdas\
-   2021 -- Java 17 LTS released\
-   2023+ -- Modern updates continue with records, switch expressions,
    etc.

### Java ME vs SE vs EE

  -----------------------------------------------------------------------
  Feature           Java ME           Java SE           Java EE
  ----------------- ----------------- ----------------- -----------------
  Target            Mobile & embedded Desktop & console Enterprise & web
                                      apps              apps

  Scope             Limited libraries Core Java APIs    Advanced APIs
                                                        (JSP, Servlets,
                                                        EJB)
  -----------------------------------------------------------------------

### JDK, JRE, JVM

-   **JVM** → Java Virtual Machine, runs Java bytecode.\
-   **JRE** → Java Runtime Environment, JVM + libraries for execution.\
-   **JDK** → Java Development Kit, includes JRE + compiler & tools for
    development.

------------------------------------------------------------------------

## 🧪 Mapping Syllabus Topics → Code

  Syllabus Topic       Where Implemented
  -------------------- ---------------------------------------------------
  Encapsulation        `Student.java` (private fields + getters/setters)
  Inheritance          `Person.java → Student.java`
  Abstraction          `Person.java (abstract)`
  Polymorphism         `TranscriptService.java`
  Interfaces           `Searchable.java`
  Singleton            `AppConfig.java`
  Builder              `Course.Builder.java`
  Streams              `CourseService.filterCourses()`
  NIO.2                `BackupService.java`
  Exception Handling   `DuplicateEnrollmentException.java`

------------------------------------------------------------------------



