---
title: "Lesson 03 - MySQL and JDBC"
---

## References

- [Tutorialspoint JDBC setup](http://www.tutorialspoint.com/jdbc/jdbc-environment-setup.htm)
- [MySQL Doc Setup](http://dev.mysql.com/doc/refman/5.7/en/tutorial.html)

## MySQL Install and Setup

- Install MySQL

    ```bash
    sudo apt install mysql
    ```

- Start MySQL

    ```bash
    mysql -h localhost -u root -p
    ```

-Note:  If you want to change root password later, you can use these commands

```bash
mysql -h localhost -u root -p
```
```mysql
UPDATE mysql.user SET Password=PASSWORD('newpassword') WHERE User='root';
FLUSH PRIVILEGES;
```

## Setting up an example Database

- Creare and use EMP database

      ```mysql
      create database EMP;
      use EMP;
      ```
- Create a table

      ```mysql
      create table Employees (
      id int not null,
      age int not null,
      first varchar (255),
      last varchar (255) );
      ```

- Add Entries

     ```mysql
     INSERT INTO Employees VALUES (100, 18, 'Zara', 'Ali');
     INSERT INTO Employees VALUES (101, 25, 'Mahnaz', 'Fatma');
     INSERT INTO Employees VALUES (102, 30, 'Zaid', 'Khan');
     INSERT INTO Employees VALUES (103, 28, 'Sumit', 'Mittal');
     ```

## Setting up JDBC

- Should already be in Cloud9's Classpath
- Create a test class with the [JDMC sample code](http://www.tutorialspoint.com/jdbc/jdbc-sample-code.htm)
