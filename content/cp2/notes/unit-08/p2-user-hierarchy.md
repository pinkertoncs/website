---
title: "Project 02 - SIS User Hierarchies"
---

## Command hierarchy

![](/images/cp2/unit-08/cmd.png)

### Administrator commands

- **create user** *usertype username password*
- **create course** *coursename*
- **create section** *coursename teacher*
- **view** *user* | *course* | *section*

### Teacher commands

- **create assignment** *coursename section# assignmentname*
- **view** *section* | *student* | *assignment*

### Student commands

- **view** *section* | *assignment*

## User data hierarchy

- Consider implementing an inheritance hierarchy for User data. For example:
    - *Admin* has a title
    - *Teacher*s have a department (A full system might include a Department class, but we will not worry about that).
    - *Student*s have a year of graduation
- Do not consider the methods listed here to be comprehensive. Add any methods you need

![](/images/cp2/unit-08/user.png)
