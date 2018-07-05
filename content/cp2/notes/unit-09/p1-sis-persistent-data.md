---
title: "Project 01 - SIS Persistent Data"
---
## Overview

- Create Data management class that allows you to read and write program data using CSV files.

## Features

- Admins should be able to :
  - Batch create new users by loading data from CSV (userdata.csv)
  - Batch create new courses by loading data from CSV (coursedata.csv)
  - Load a course roster from CSV.
- Teachers should be able to:
  - Export gradebook to CSV

## Specifications
- When you're implementing this, you'll have to think carefully about the order of operations
for saving and restoring the system.  For example:
    - What happens if you try to load the course data and rosters before you've loaded the user
    data?
- These questions must be considered, and you can't assume that the user will always follow
directions!

#### Data commands

- Admin:
  - ```load users|courses <filename>```
  - ```load roster <coursename> <filename>```

#### Data files

- The data file format will depend on the data you're storing, but will require at least this:
- **userdata.csv**, 1 user specified per line
  - usertype, username, password
- **coursedata.csv**, 1 course specified per line, with optional section specifications
  - coursename [, section#, teachername, studentname*]
- **roster.csv**: 1 username per line
  - username
