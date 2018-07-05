---
title: "Project 02 - SIS Data Models"
---

- The data subsystem of the SIS consists of the following
    - **Database**: container for Users and Courses
    - **Course**: container for **Section**
    - **User** and **Section** have a many-to-many relationship (ENROLLED) and a 1-to-1 relationship (TEACHES)
- Note that the fields / methods lists in this diagram are examples and should not be considered complete.

![](/images/cp2/unit-07/data-models.png)

## Testing / Requirements

- You should have some unit testing for each of these classes.
- Your primary testing for this subsystem will be in the Database class
- When Mr. K. grades this he will run your Database class main function, so you should have extensive testing, including:
    - Creating, reading, updating, and deleting Courses, Users, and Sections
    - Assigning a User to a Section as a Teacher
    - Enrolling a User in a Section
