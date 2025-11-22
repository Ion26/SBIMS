Student Branch Information Management System (SBIMS)

Build Your Own Project – Project Report
Author: Ayan Shams
University: VIT Bhopal
Course: CSE – Build Your Own Project
Year: 2025
Reg. no. 25BHI10082
1. Introduction

In modern educational institutions, efficient management of student data is essential. Large numbers of students spread across different branches make manual record-keeping difficult, error-prone, and time-consuming.

This project, Student Branch Information Management System (SBIMS), is a modular Python application designed to simplify and streamline the management of student information using a command-line interface and CSV-based storage.

2. Problem Statement

Manual management of student records becomes increasingly challenging as student numbers grow. Information such as name, branch, year, GPA, and email is scattered or stored in unstructured formats, making operations like searching, sorting, updating, and analyzing tedious and inefficient.

SBIMS aims to solve these issues by offering a centralized digital management system with CRUD operations and basic analytics.

3. Objectives

To develop a modular and scalable system for managing student data

To implement CRUD operations on student records

To provide easy search, filter, and analytical functionalities

To ensure a user-friendly interaction through a command-line menu

To demonstrate clean Python coding practices and modular structure

4. Functional Requirements

The system provides the following functionalities:

Add Student – Add a new student record

List Students – Display all students

Search by Name – Partial match search across names

Filter by Branch – Display only students belonging to a specific branch

Top N Students – View highest-GPA students

Update Student – Modify existing student information

Delete Student – Remove a student by ID

Branch Distribution – Number of students per branch

Average GPA per Branch – Compute branch-wise GPA averages

5. Non-Functional Requirements

Usability: Simple text-based interface

Maintainability: Modular file structure (input, process, analytics, model, storage)

Performance: CSV operations optimized with minimal overhead

Scalability: New modules or analytics can be added easily

Reliability: Validations to prevent invalid entries

Portability: Runs on any system with Python installed

6. System Architecture

The system follows a modular pipeline:

User
  ↓
Main Menu (main.py)
  ↓
Modules
  ↓
CSV Storage (students.csv)


Modules:

student_model.py → Defines Student class

storage.py → Read/write CSV

input_module.py → Add/List/Update/Delete

process_module.py → Search/Filter/Top N

analytics_module.py → Distribution & GPA stats

7. Design Diagrams
7.1 Use Case Diagram
         +--------------+
         |    Admin     |
         +--------------+
                |
        ----------------------
        |    |     |     |  |
 Add   List Search Filter Analytics

7.2 Workflow Diagram
Start → Show Menu → Get Input → Perform Operation → Back to Menu → Exit

7.3 Sequence Diagram (Add Student)
User → main.py → input_module → storage → CSV File  

7.4 Class Diagram
Student
 ├── sid
 ├── name
 ├── branch
 ├── year
 ├── gpa
 └── email

7.5 Component Diagram
main.py  
  ├── input_module  
  ├── process_module  
  ├── analytics_module  
  └── storage

8. Implementation Details

The project is implemented entirely in Python.

Student data is stored in students.csv.

Each module handles a specific type of functionality.

Menu-driven navigation makes usage simple and intuitive.

Error handling prevents invalid entries.

9. Screenshots / Results

(Add your screenshots here, for example:)

Adding a student

Listing students

Analytics output

Search/Filter results
(You can take screenshots from the VS Code terminal.)

10. Testing Approach
Manual Testing

Verified adding, listing, searching, filtering, updating, deleting

Verified CSV correctness

Verified analytics output

Checked behavior with empty fields and invalid inputs

Automated Testing (optional)

Test cases can be added using pytest

11. Challenges Faced

Understanding the modular structure at the beginning

Managing CSV formatting properly

Debugging module import paths

Handling Python interpreter issues in VS Code

12. Learnings & Key Takeaways

Learned how to divide a project into modules

Understood CRUD operations & CSV handling

Gained confidence in building full applications

Improved debugging and Python programming skills

13. Future Enhancements

Add authentication/login

Migrate to SQLite/SQL database

Add GUI using Tkinter or a web UI with Flask

Add graph-based analytics

Add student ID validation

14. Conclusion

SBIMS successfully demonstrates a modular student management system capable of handling core academic data operations effectively.
It meets all the functional and non-functional requirements described in the assignment and provides a strong foundation for further extension.

15. References

Python Documentation

VIT “Build Your Own Project” PDF

StackOverflow (for debugging imports)

CSV module documentation