# DATABASE SYSTEM CONCEPTS
The landscape of computer science education has undergone a profound transformation in recent years, as database management has emerged as a critical pillar in modern computing environments. To equip students with the essential knowledge about database systems, we present a comprehensive exploration of the fundamental concepts of database management, ranging from database design to database languages to database-system implementation.

Intended for students at the junior or senior undergraduate or first-year graduate level, this text provides both basic materials for an introductory course as well as advanced material suitable for supplemental or advanced study. Assuming only a familiarity with basic data structures, computer organization, and high-level programming languages like Java, C, or Pascal, we present concepts as intuitive descriptions, grounded in the running example of a university.

While important theoretical results are covered, we eschew formal proofs in favor of figures and examples that vividly illustrate the truth of a given result. Formal descriptions and proofs can be found in advanced texts and research papers referenced in the bibliographical notes.

This repository is an indispensable resource for anyone seeking to acquire a deep understanding of database management, rooted in theoretical foundations but connected to practical applications.

## Content

[**Introduction**](https://github.com/DabovS/Database-System-Concepts#introduction)

[**RELATIONAL DATABASES**](https://github.com/DabovS/Database-System-Concepts#relational-databases-1)

[*Introduction to the Relational Model*](https://github.com/DabovS/Database-System-Concepts#introduction-to-the-relational-model)

[*Introduction to SQL*](https://github.com/DabovS/Database-System-Concepts#introduction-to-sql)

[*Intermediate SQL*](https://github.com/DabovS/Database-System-Concepts#intermediate-sql)

[*Advanced SQL*](https://github.com/DabovS/Database-System-Concepts#advanced-sql)

[*Formal Relational Query Languages*](https://github.com/DabovS/Database-System-Concepts#formal-relational-query-languages)

[**DATABASE DESIGN**](https://github.com/DabovS/Database-System-Concepts/blob/main/README.md#database-design-1)

[*Database Design and the E-R Model*](https://github.com/DabovS/Database-System-Concepts/blob/main/README.md#database-design-and-the-e-r-model)

[*Relational Database Design*](https://github.com/DabovS/Database-System-Concepts/blob/main/README.md#relational-database-design)

[*Application Design and Development*](https://github.com/DabovS/Database-System-Concepts/blob/main/README.md#application-design-and-development)

[**DATA STORAGE AND QUERYING**](https://github.com/DabovS/Database-System-Concepts#data-storage-and-querying-1)

[*Storage and File Structure*](https://github.com/DabovS/Database-System-Concepts#storage-and-file-structure)

[*Indexing and Hashing*](https://github.com/DabovS/Database-System-Concepts#indexing-and-hashing)

[*Query Processing*](https://github.com/DabovS/Database-System-Concepts#query-processing)

[*Query Optimization*](https://github.com/DabovS/Database-System-Concepts#query-optimization)

[**TRANSACTION MANAGEMENT**](https://github.com/DabovS/Database-System-Concepts#transaction-management-1)

[*Transactions*](https://github.com/DabovS/Database-System-Concepts#transactions-1)

[*Concurrency Control*](https://github.com/DabovS/Database-System-Concepts#concurrency-control)

[*Recovery System*](https://github.com/DabovS/Database-System-Concepts#recovery-system)

[**SYSTEM ARCHITECTURE**](https://github.com/DabovS/Database-System-Concepts/blob/main/README.md#system-architecture)

[*Database-System Architectures*](https://github.com/DabovS/Database-System-Concepts/blob/main/README.md#database-system-architectures)

[*Parallel Databases*](https://github.com/DabovS/Database-System-Concepts/blob/main/README.md#parallel-databases)

[*Distributed Databases*](https://github.com/DabovS/Database-System-Concepts/blob/main/README.md#distributed-databases)

[**DATA WAREHOUSING, DATA MINING, AND INFORMATION RETRIEVAL**](https://github.com/DabovS/Database-System-Concepts/blob/main/README.md#data-warehousing-data-mining-and-information-retrieval)

[*Data Warehousing and Mining*](https://github.com/DabovS/Database-System-Concepts/blob/main/README.md#data-warehousing-and-mining)

[*Information Retrieval*](https://github.com/DabovS/Database-System-Concepts/blob/main/README.md#information-retrieval)

[**SPECIALTY DATABASES**](https://github.com/DabovS/Database-System-Concepts/blob/main/README.md#specialty-databases-1)

[*Object-Based Databases*](https://github.com/DabovS/Database-System-Concepts/blob/main/README.md#object-based-databases)

[*XML*](https://github.com/DabovS/Database-System-Concepts/blob/main/README.md#xml)


[**ADVANCED TOPICS**](https://github.com/DabovS/Database-System-Concepts/blob/main/README.md#advanced-topics)

[*Advanced Application Development*](https://github.com/DabovS/Database-System-Concepts/blob/main/README.md#advanced-application-development)

[*Spatial and Temporal Data and Mobility*](https://github.com/DabovS/Database-System-Concepts/blob/main/README.md#spatial-and-temporal-data-and-mobility)

[*Advanced Transaction Processing*](https://github.com/DabovS/Database-System-Concepts/blob/main/README.md#advanced-transaction-processing)

# Introduction


### Database-System Applications 
Database management systems (DBMS) is a system that stores and manages data, with the goal of providing a way to store and retrieve database information that is both convenient and efficient. Databases are used in many applications such as enterprise information, banking and finance, universities, airlines, and telecommunications. In addition to these applications, databases also play an important role in everyday life, such as when accessing an online bookstore, bank website, or viewing advertisements online. Database systems are designed to manage large bodies of information, ensuring the safety of information stored, despite system crashes or attempts at unauthorized access. The purpose of database systems  is to provide a more efficient way to manage commercial data compared to earlier methods such as storing it in operating system files.

### Purpose of Database Systems 
The disadvantages of keeping organizational information in a file-processing system, highlighting the issues of data redundancy, difficulty in accessing data, data isolation, integrity problems, atomicity problems, and concurrent-access anomalies, these problems can lead to higher storage and access costs, data inconsistency, and data loss, and can make it difficult to maintain data consistency, supervise data access, and provide responsive data-retrieval systems. As a result, more responsive and efficient data-retrieval systems are required.

### View of Data 
The development of database systems to solve problems with file-processing systems is a collection of interrelated data and programs that allow users to access and modify the data. The system provides users with an abstract view of the data by using multiple levels of abstraction, including the physical level, logical level, and view level. The physical level describes how the data are stored, while the logical level describes what data are stored and what relationships exist among those data. The view level describes only part of the database to simplify users' interactions with the system. Many users of the database system do not need all the information stored in the database, and the view level of abstraction exists to simplify their interaction with the system.

![1](https://user-images.githubusercontent.com/124214430/226368719-f3e28a11-3b05-4413-ae7e-fb8cffcb7752.png)

```
Type instructor = record
        ID : char (5); 
        name : char (20); 
        dept name : char (20); salary : numeric (8,2);
    end;
```
The code defines a new record type called "instructor" with four fields, each having a name and type. A university may have other record types, such as "department," "course," and "student," each with their own fields. At the physical level, each record is stored as a block of consecutive storage locations, but this detail is hidden from programmers and database users. Database administrators may be aware of these physical details.

At the logical level, records are described by type definitions and their interrelationships are defined. Programmers and database administrators work at this level. At the view level, computer users see application programs that hide details of the data types. Views of the database are defined to provide a security mechanism to prevent users from accessing certain parts of the database.

The overall design of a database is called the database schema, while the information stored in the database at a particular moment is called an instance of the database. There are different types of schemas, such as the physical schema, logical schema, and view level schema. The logical schema is the most important as programmers use it to construct applications. The different data models used in databases are the relational model, entity-relationship model, object-based data model, and semistructured data model. The relational model is the most widely used. The network data model and the hierarchical data model are used little now and are outlined in appendices for interested readers.

### Database Languages 
The two main languages used in a database system are the data-manipulation language (DML) and the data-definition language (DDL). The DML allows users to access, insert, delete and modify data stored in the database. It can be either procedural or declarative, with the latter being easier to use but requiring the system to figure out how to access data. A query language is a part of DML that involves information retrieval. SQL is the most widely used query language.

The DDL specifies the database schema and additional properties of the data. It is also used to define the storage structure and access methods. The DDL includes constraints such as domain constraints, referential integrity, assertions, and authorization. These constraints ensure the consistency of data and restrict the type of access users have on various data values in the database. 

### Relational Databases 
Relational databases are using tables to represent data and relationships among that data. Each table has multiple columns with unique names, and record-based models organize data in fixed-format records of several types. SQL is the most common language used in commercial relational database systems, and it covers it in detail in Chapters 3, 4, and 5. The relational model can have schema design problems, such as unnecessarily duplicated information, which are discussed in Chapter 8.

![2](https://user-images.githubusercontent.com/124214430/226368671-27302650-6467-40e8-9c16-dcb4bd717ca8.png)

![3](https://user-images.githubusercontent.com/124214430/226368646-cd079b0f-f70f-4be0-9c4e-ba3c93e5c5ee.png)

The Data-Manipulation Language (DML) used in relational databases above, specifically the nonprocedural SQL query language. A query takes input from one or more tables and always returns a single table. An example SQL query is provided to illustrate how to retrieve data from a table.

```
            select instructor.name 
            from instructor 
            where instructor.dept name = ’History’;
```

The expected result of running a specific SQL query on the tables in Figure 1.2. The query is designed to find the names of all instructors in the History department. The system would search the tables and find that there are two departments with a budget greater than $95,000: Computer Science and Finance. There are a total of five instructors in these departments, so the resulting table would have two columns (ID, dept name) and five rows listing the instructors in the two departments.

```
Create table department
        (dept, name char (20), 
        building char (15),
        budget  numeric (12,2));
```

The Data-Definition Language (DDL) in SQL allows for the definition of tables and other database elements. The schema of a table is an example of metadata. SQL is not as powerful as a universal Turing machine and cannot support actions like input from users or output to displays, so application programs must be written in a host language like C, C++, or Java. DML statements can be executed from the host language either by providing an application program interface or by embedding DML calls within the host language program using a preprocessor like the DML precompiler.

### Database Design and Data Storage and Querying 
Database design involves managing large amounts of information that are part of an enterprise's operation. The initial step in designing a database is to characterize fully the data needs of prospective database users. Next, a data model is chosen and the requirements are translated into a conceptual schema. The designer reviews the schema to confirm that all data requirements are satisfied and are not in conflict with one another. The final design phases involve mapping the conceptual schema onto the implementation data model of the database system that will be used and specifying the physical features of the database. An example of how a database for a university could be designed. The entity-relationship data model is discussed as a way to represent entities and relationships in a database.

![4](https://user-images.githubusercontent.com/124214430/226368609-4528b6b0-4cfc-4dfa-b879-27a51dbf27b3.png)

Two methods for designing a relational database: entity-relationship modeling and normalization. Entity-relationship modeling involves representing entity sets and relationship sets using UML, while normalization aims to generate relation schemas that avoid redundancy and allow easy information retrieval. Also, how-to map correctly cardinalities in the E-R model and discusses the drawbacks of a poorly designed database, such as repetition of information and an inability to represent certain information.

![5](https://user-images.githubusercontent.com/124214430/226368552-380eaa34-9ab1-4aea-aa66-7d5674771bb6.png)

### Transaction Management 
Two problems arise when designing databases, namely, the repetition of information and the inability to represent certain information. These problems can be resolved through normalization, which is a formal method of designing databases. The passage also explains the two main components of a database system, the storage manager, and the query processor. The storage manager is responsible for storing, retrieving, and updating data in the database, and its components include the authorization and integrity manager, transaction manager, file manager, and buffer manager. The query processor, on the other hand, simplifies access to data for database users. The passage also discusses the importance of minimizing the movement of data between disk and main memory, as well as the different data structures implemented by the storage manager, including data files, data dictionary, and indices.

### Database Architecture
**The three main components:**

* Query Processor
* Transaction Management
* Database Architecture

![6](https://user-images.githubusercontent.com/124214430/226368517-21c7c867-64db-4e9b-981c-7d5e67596a52.png)

**The Query Processor consists of three parts:**

* DDL Interpreter
* DML Compiler
* Query Evaluation Engine

The DDL Interpreter interprets DDL statements and records the definitions in the data dictionary. The DML Compiler translates DML statements in a query language into an evaluation plan consisting of low-level instructions. The Query Evaluation Engine executes low-level instructions generated by the DML Compiler. Transaction Management deals with the processing of a single logical function in a database application called a transaction, which must satisfy atomicity, consistency, and durability properties. The Recovery Manager ensures the atomicity and durability properties of a transaction, while the Concurrency Control Manager controls the interaction among concurrent transactions to ensure the consistency of the database. 

![7](https://user-images.githubusercontent.com/124214430/226368459-5bcce428-f6bc-4ceb-9d26-1ba5faa356c3.png)

The Database Architecture is greatly influenced by the underlying computer system on which the database system runs, and it includes centralized, client-server, parallel, and distributed databases. The book covers the general structure of modern computer systems, how various actions of a database can be implemented to exploit parallel processing, and how to deal with issues that arise in a distributed database.

### Data Mining and Information Retrieval and Specialty Databases 
Data mining is the process of analyzing large databases to find useful patterns, and information retrieval, which is the querying of unstructured textual data. Specialty databases, such as object-based data models and semistructured data models. Object-oriented programming concepts, such as encapsulation and inheritance, have been applied to data modeling. The object-relational data model is a combination of object-oriented and relational models. Semistructured data models allow for data with varying sets of attributes and are used in XML language. Chapters 20 to 23 cover these topics in more detail.

### Database Users and Administrators
The different types of users who work with a database system, including users, application programmers, sophisticated users, and specialized users. Each type of user interacts with the system differently, using various user interfaces and tools. Additionally, the text explains the role of a database administrator (DBA), who has central control over the system, including creating and modifying the database schema, granting authorization for data access, and performing routine maintenance tasks like backing up the database and monitoring performance.

### History of Database Systems 
The use of punched cards and mechanical systems were the precursors to automation of data processing tasks. In the late 1960s and 1970s, the use of hard disks led to the creation of network and hierarchical databases, and the introduction of the relational model by Codd. Although the relational model was not initially used due to perceived performance disadvantages, it became dominant in the 1980s. The 1990s saw the explosive growth of the World Wide Web, which necessitated database systems that supported high transaction-processing rates, reliability, and 24x7 availability. The 2000s saw the growth of XML and associated query language XQuery, as well as autonomic-computing/auto-admin techniques, and the use of open-source database systems like PostgreSQL and MySQL. The latter part of the decade saw the growth of specialized databases for data.

# RELATIONAL DATABASES
The importance of data models, with a focus on the relational model. The relational model uses tables to represent data and relationships, and is widely adopted in database products. To make data available to users, query languages like SQL have been developed, and data integrity and protection are also important issues. Chapters 3, 4, and 5 cover SQL, including integrity constraints and authorization mechanisms. Chapter 6 covers formal query languages based on mathematical logic, which form the basis for SQL and other user-friendly languages.

## Introduction to the Relational Model and Structure of Relational Databases
The relational model is the primary data model for commercial data-processing applications because of its simplicity. It is made up of a collection of tables, where each table is assigned a unique name and consists of rows and columns. 

![8](https://user-images.githubusercontent.com/124214430/226383016-532340b9-c340-482a-95a5-22cb11507604.png)

A row in a table represents a relationship among a set of values, and each table is a collection of relationships. In the relational model, a relation is used to refer to a table, while the term tuple is used to refer to a row, and the term attribute refers to a column of a table. 

![9](https://user-images.githubusercontent.com/124214430/226383067-345b1bed-c27e-461d-861a-fd75493d995d.png)

![10](https://user-images.githubusercontent.com/124214430/226383096-82e90618-8cdd-42fa-9bf5-00488a344202.png)

Each attribute of a relation has a set of permitted values, called the domain of that attribute. The null value is a special value that signifies that the value is unknown. This chapter focuses on the fundamentals of the relational model, including the structure of relational databases, and the correspondence between the concept of a table and the mathematical concept of a relation.

![11](https://user-images.githubusercontent.com/124214430/226383117-c060c33c-85fa-4c5c-a1b0-3915ef02c819.png)

### Database Schema
The concept of database schema refers to the logical design of a database, and the database instance, which is a snapshot of the data in the database at a given instant in time. A relation schema consists of a list of attributes and their corresponding domains, while a relation instance corresponds to the value of a variable. 

![12](https://user-images.githubusercontent.com/124214430/226383163-4da92df0-5db2-42a6-8d0d-3f6a48769ba9.png)

```
department (dept name, building, budget)

```

The schema of a relation generally does not change, whereas the contents of a relation instance may change as the relation is updated. 

```
section (course id, sec id, semester, year, building, room number, time slot id)
```

Common attributes in relation schemas are used to relate tuples of distinct relations. 

```
teaches (ID, course id, sec id, semester, year)
```

![13](https://user-images.githubusercontent.com/124214430/226383188-00ae03bc-aeeb-4f92-8e1b-f5d2bf207f35.png)

Examples of different relation schemas and instances in a university database.

* student (ID, name, dept name, tot cred)
* advisor (s id, i id)
* takes (ID, course id, sec id, semester, year, grade)
* classroom (building, room number, capacity)
* time slot (time slot id, day, start time, end time)

![14](https://user-images.githubusercontent.com/124214430/226383219-31fe4fa6-3d10-442c-8b1c-7aa5ce1c6612.png)

### Keys
The concept of keys in database design is important for identifying tuples within a relation. A superkey is a set of one or more attributes that can uniquely identify a tuple in the relation, while a candidate key is a minimal superkey for which no proper subset is a superkey. A primary key is a candidate key chosen by the database designer as the principal means of identifying tuples within a relation. Primary keys should be chosen carefully, as they represent a constraint in the real-world enterprise being modeled, and should be unlikely to change. Foreign keys are attributes in a relation that reference the primary key of another relation. Referential integrity constraints require that the values appearing in specified attributes of any tuple in the referencing relation also appear in specified attributes of at least one tuple in the referenced relation.

### Schema Diagrams
Schema diagrams are used to depict the structure of a database schema, including primary key and foreign key dependencies. Each relation is represented as a box with the relation name and attributes listed inside, and foreign key dependencies are shown as arrows. Other referential integrity constraints are not shown explicitly, but can be represented using entity-relationship diagrams. Many database systems provide graphical tools for creating schema diagrams. The example organization used in later chapters is a university, and its corresponding relational schema is provided in Figure 15.

![15](https://user-images.githubusercontent.com/124214430/226383272-93f8b3fa-6a57-43ce-bb57-4ea1a48c9d16.png)

### Relational Query Languages
Query languages used to retrieve information from a database  can be procedural or nonprocedural. SQL is a widely used query language that incorporates elements of both approaches. Also, "pure" query languages are related to  the relational algebra, tuple relational calculus, and domain relational calculus. These languages are formal and lack the "syntactic sugar" of commercial languages but illustrate fundamental techniques for extracting data from a database. The relational algebra consists of a set of operations, while the relational calculus uses predicate logic to define desired results without giving specific procedures.

![16](https://user-images.githubusercontent.com/124214430/226383300-87669b52-de04-4ef3-9b96-05e104b4787b.png)

### Relational Operations
Relational operations are a set of operations that can be applied to either a single relation or a pair of relations. The most frequent operation is selecting specific tuples from a single relation that satisfies a particular predicate.

![17](https://user-images.githubusercontent.com/124214430/226383333-7502f63a-a381-4d1a-a01c-fac572ae6d99.png)

Another operation is selecting certain attributes from a relation. The join operation combines two relations by merging pairs of tuples, and the natural join operation matches tuples whose values are the same on all attribute names that are common to both relations. 

![18](https://user-images.githubusercontent.com/124214430/226383358-5bab3e69-760e-47fd-9951-59a7d379e540.png)

![19](https://user-images.githubusercontent.com/124214430/226383369-448e76fc-52c3-4d30-8d83-088dac09eeef.png)

The Cartesian product operation combines tuples from two relations, regardless of whether their attribute values match. Normal set operations like union, intersection, and set difference can be performed on relations. Operations can be performed on the results of queries.

![20](https://user-images.githubusercontent.com/124214430/226383407-0d96a0b8-22df-40aa-ae67-82586177c6ee.png)

## Introduction to SQL
The chapter discusses various database query languages but focuses on the widely used SQL language. SQL can do more than just querying a database; it can also define data structure, modify data, and specify security constraints. The chapter covers SQL's fundamental concepts and constructs and acknowledges that individual SQL implementations may differ in details or support only a subset of the full language.


### Overview of the SQL Query Language 
The SQL language was originally developed by IBM in the 1970s and has evolved into the standard relational database language. ANSI and ISO have published several versions of the SQL standard, including SQL-86, SQL-89, SQL-92, SQL:1999, SQL:2003, SQL:2006, and SQL:2008. The SQL language consists of various parts, including DDL, DML, integrity, view definition, transaction control, embedded SQL and dynamic SQL, and authorization. The chapter presents an overview of basic DML and DDL features of SQL, while Chapters 4 and 5 cover more advanced features. Although most SQL implementations support standard features, differences between implementations exist, and users should consult their database system's user manuals to determine which features are supported.


### SQL Data Deﬁnition 
This passage discusses the importance of specifying the set of relations in a database through a data-definition language (DDL), and explains the different components that can be defined using SQL DDL, including the schema, types of values, integrity constraints, indices, security, and physical storage structure. The passage then goes on to describe the basic types supported by SQL, including char, varchar, int, smallint, numeric, real, double precision, and float. The concept of null values is also introduced. Finally, the passage discusses the differences between char and varchar types and recommends using varchar to avoid problems with extra spaces. The nvarchar type for storing multilingual data using Unicode representation is also briefly mentioned, as well as basic schema definition.

We deﬁne an SQL relation by using the create table command. The following command creates a relation department in the database.

```
create table department
(dept name varchar (20), 
building varchar (15), 
budget numeric (12,2),
primary key (dept name));
```

An example of creating a relation in SQL with three attributes - dept name, building, and budget. The data types for these attributes are specified as character string of maximum length 20, character string of maximum length 15, and number with 12 digits in total, 2 of which are after the decimal point, respectively. The primary key for this relation is set to be the dept name attribute.

```
create table r 
        (A1 D1, 
        A2 D2, 
        ...,
        An Dn,
        (integrity-constraint1), 
        ...,
        (integrity-constraintk));
```

* SQL commands and constraints, the syntax of creating tables and defines various constraints such as primary key, foreign key, and not null. 
* SQL prevents any updates to the database that violate an integrity constraint.
* For exampleL insert command used to load data into a relation. 
* Also, refers to a partial SQL DDL definition of the university database.

We can use the delete command to delete tuples from a relation:

![21](https://user-images.githubusercontent.com/124214430/228469151-30a793a5-f4d5-47df-b576-368c1d99c400.png)

The delete command in SQL can be used to remove specific tuples from a relation or all tuples from the relation. The drop table command is used to remove a relation from the SQL database, deleting all information about it:

```
drop table r;
```

```
delete from r;
```

*   SQL commands for modifying the structure of a relation, including deleting tuples or dropping a relation entirely using the DELETE and DROP TABLE commands, respectively. 
*   The ALTER TABLE command for adding attributes to an existing relation, with all tuples assigned null as the value for the new attribute.

```
alter table r add AD;
```

The alter table command allows us to add a new attribute to an existing relation named r, where A is the name of the attribute to be added and D is the type of the new attribute. In contrast, we can remove attributes from a relation using the drop command.

```
alter table r drop A;
```
In SQL, an attribute can be dropped from an existing relation by using the *alter table* command. However, many database systems do not support this functionality, and instead only allow an entire table to be dropped.

### Basic Structure of SQL Queries 

The basic structure of an SQL query consists of three clauses: select, from, and where. The query operates on the relations listed in the from clause, performs operations on them as specified in the where and select clauses, and produces a relation as the result.

![22](https://user-images.githubusercontent.com/124214430/228469256-9c55d23e-d479-4fa6-9d8a-b126c14f47ba.png)

In the case of a query on a single relation, the example given is to find the names of all instructors in the university example. The instructor relation is listed in the from clause and the name attribute is specified in the select clause.

```
select name 
from instructor;
```

The basic structure of an SQL query consists of three clauses: select, from, and where. The select clause specifies the attributes of the relation to be displayed in the output, the from clause specifies the input relation, and the where clause is used for filtering the tuples. 


```
select dept name
from instructor;
```

SQL allows duplicate tuples in relations and in the results of SQL expressions. In order to force the elimination of duplicates, the keyword "distinct" is inserted after select.

```
select distinct dept name 
from instructor;
```

![23](https://user-images.githubusercontent.com/124214430/228469303-8d089028-869e-4cd3-bbf6-c15f57cb07ad.png)

The SQL keyword "distinct" can be used to eliminate duplicates in query results, while "all" can be used to specify that duplicates should be retained. The select clause in SQL queries can include arithmetic expressions that involve mathematical operators and constants or attributes of tuples. 

```
select all dept name 
from instructor;
```

The where clause allows the selection of specific rows in the query result based on a specified predicate.

```
select ID, name, dept name, salary *1.1 
from instructor;
```

The SQL language allows us to manipulate data in a relational database. We can use arithmetic expressions to modify the values of attributes or create new attributes, but this does not modify the original relation. 

![24](https://user-images.githubusercontent.com/124214430/228469344-a8975781-6fae-4f34-84b7-50f40ca5d6c8.png)

```
select name 
from instructor 
where dept name = ’Comp. Sci.’ and salary > 70000;
```

SQL also provides special data types and arithmetic functions to operate on them. We can use the WHERE clause to filter the results of a query and retrieve only those tuples that satisfy a specified predicate. 

![25](https://user-images.githubusercontent.com/124214430/228469380-10560e40-0ac5-4ea1-a500-816d2ceac65a.png)

Logical connectives such as AND, OR, and NOT can be used in the WHERE clause along with comparison operators to compare strings and arithmetic expressions. In queries involving multiple relations, we need to specify the relations to be accessed in the FROM clause and specify the matching condition in the WHERE clause. The SELECT clause is used to retrieve the desired attributes from the selected tuples.

This section discusses SQL queries that involve multiple relations. It explains that in such cases, the naming convention requires that relations in the from clause have distinct names. The select clause is used to list the desired attributes in the query result, the from clause is a list of the relations to be accessed, and the where clause is a predicate involving attributes of the relations in the from clause. The general form of an SQL query is given, which includes attributes, relations, and a predicate. If the where clause is omitted, the predicate is true.

```
select A1, A2,..., An 
from r1, r2,...,rm 
where P;
```

The order of the clauses in an SQL query must be select, from, and then where, but it can be easier to understand the operations if they are considered in the order from, where, and then select. The from clause generates tuples for the result relation of the from clause by defining a Cartesian product of the relations listed in the clause. 

```
for each tuple t1 in relation r1 
    for each tuple t2 in relation r2
        ... 
            for each tuple tm in relation rm
                Concatenate t1, t2,..., tm into a single tuple t
                Add t into the result relation
```

This is done iteratively, creating a new tuple by concatenating each tuple in each relation, and then adding that tuple to the result relation. The result relation has all attributes from all the relations in the from clause, and since the same attribute name may appear in multiple relations, the name of the relation from which the attribute originally came must be prefixed before the attribute name.

The naming convention used in SQL queries involving multiple relations:

```
(instructor.ID, instructor.name, instructor.dept name, instructor.salary teaches.ID, teaches.course id, teaches.sec id, teaches.semester, teaches.year)
```

Attributes that appear in only one relation do not need to be pre-fixed with the relation name. However, when the same attribute name appears in multiple relations, the naming convention requires that the attribute be prefixed with the relation name to avoid ambiguity. 

```
(instructor.ID, name, dept name, salary teaches.ID, course id, sec id, semester, year)
```

The Cartesian product of relations is defined as a set of tuples generated by iterating through each tuple in each relation listed in the from clause. The resulting relation has all the attributes from all the relations in the from clause. The article illustrates the Cartesian product of the instructor and teaches relations and explains that combining tuples from unrelated relations can result in an extremely large relation, making it rarely sensible to create such a Cartesian product.

![26](https://user-images.githubusercontent.com/124214430/228469433-26cd5483-2267-4a9f-ae47-3a13f146ef6b.png)

To use the WHERE clause in an SQL query to restrict the output to meaningful results. The WHERE clause is used to combine tuples from different tables based on common attributes. 

```
select name, course id 
from instructor, teaches 
where instructor.ID= teaches.ID;
```


SQL query combines tuples from the instructor and teaches tables to output instructor names and course IDs. The output only includes instructors who have taught some course, and instructors who have not taught any course are excluded. 

```
select name, course id 
from instructor, teaches 
where instructor.ID= teaches.ID and instructor.dept name = ’Comp. Sci.’;
```

To add an extra predicate to the WHERE clause to further restrict the output:

![27](https://user-images.githubusercontent.com/124214430/228469489-31b44bc7-df6e-4307-9ae1-d37e16904a26.png)

The sequence of steps involved in executing an SQL query, which involves generating a Cartesian product of the relations listed in the FROM clause, applying predicates specified in the WHERE clause, and outputting the selected attributes. However, a real implementation of SQL optimizes the evaluation process to generate only the elements of the Cartesian product that satisfy the WHERE clause predicates. Also the consequences of omitting appropriate WHERE clause conditions can lead to the output of a huge relation.

The natural join operation in SQL produces a relation as a result by considering only those pairs of tuples with the same value on the common attributes that appear in the schemas of both relations. SQL also supports other ways of joining information from multiple relations.

![28](https://user-images.githubusercontent.com/124214430/228469544-ebdabc23-180d-48c3-8c64-883429eb894a.png)

The natural join operation in SQL combines information from two relations based on the matching of attributes with the same name. 

```
select name, course id 
from instructor, teaches 
where instructor.ID= teaches.ID;
```

It produces a relation that contains only those tuples with the same value on the common attribute. 

```
select name, course id 
from instructor natural join teaches;
```

The resulting relation has only those attributes that are common to the schemas of both relations, followed by those that are unique to the schema of each relation.

```
select A1, A2,..., An 
from r1 natural join r2 natural join ... natural join rm 
where P;
```

The natural join can be used in SQL queries with the from clause to combine multiple relations. 

```
from E1, E2,..., En
```

The select and where clauses are then evaluated on the resulting relation. 

```
select name, title 
from instructor natural join teaches, course 
where teaches.course id= course.course id;
```

The natural join is a useful tool for simplifying SQL queries and reducing the size of the output.

SQL operations, specifically natural join and rename operations. 

```
select name, title 
from instructor natural join teaches natural join course;
```

```
select name, title 
from (instructor natural join teaches) join course using (course id);
```

### Additional Basic Operations 

```
select name, course id 
from instructor, teaches 
where instructor.ID= teaches.ID
```

```
name, course id
```

The natural join operation combines two tables by matching attributes with the same name, while the rename operation allows renaming of table attributes using the "as" clause. 

```
name, course id
```

```
old-name as new-name
```

Natural join while avoiding equating attributes erroneously and how the rename operation is useful in renaming relations. 

```
select name as instructor name, course id from instructor, teaches 
where instructor.ID= teaches.ID;
```

```
select T.name, S.course id 
from instructor as T, teaches as S 
where T.ID= S.ID;
```

SQL queries use these operations to obtain specific results.

SQL queries and a few examples below of different operations that can be performed on character strings:

```
select distinct T.name 
from instructor as T, instructor as S 
where T.salary > S.salary and S.dept name = ’Biology’;
```

Also, the use of correlation names or table aliases in SQL. SQL strings are enclosed in single quotes and that the equality operation on strings is case sensitive. 

```
select dept name 
from department 
where building like ’%Watson%’;
```

SQL also permits a variety of functions on character strings, such as concatenation, substring extraction, and string length calculation. To perform pattern matching using the like operator and how to specify an escape character for special pattern characters.

```
like ’ab\%cd%’ escape ’\’ matches all strings beginning with “ab%cd”
like ’ab\\cd%’ escape ’\’ matches all strings beginning with “ab\cd”

```

Finally, some databases provide variants of the like operation which do not distinguish between lower and upper case, and SQL:1999 offers a similar to operation that provides more powerful pattern matching.

In SQL, the asterisk symbol (*) is used in the select clause to indicate "all attributes" of a table.

```
select instructor.* 
from instructor, teaches 
where instructor.ID= teaches.ID;
```

The order by clause can be used to sort the tuples in the result of a query in ascending or descending order, and can be performed on multiple attributes. 

```
select name 
from instructor 
where dept name = ’Physics’ order by name;
```

The between comparison operator simplifies where clauses that specify a value range, and the not between operator can also be used. 

```
select * 
from instructor 
order by salary desc, name asc;
```

To find instructor names and the courses they taught for instructors in the Biology department who have taught some course, an extra condition can be added to the where clause.

```
select name 
from instructor 
where salary between 90000 and 100000;
```

instead of:

```
select name 
from instructor 
where salary <= 100000 and salary >= 90000;
```

Below are various SQL operations such as attribute specification, ordering of tuples, where clause predicates, and set operations:

```
select name, course id 
from instructor, teaches 
where instructor.ID= teaches.ID and dept name = ’Biology’;
```

```
select name, course id 
from instructor, teaches 
where (instructor.ID, dept name) = (teaches.ID, ’Biology’);
```
```
select name, course id 
from instructor, teaches 
where (instructor.ID, dept name) = (teaches.ID, ’Biology’);
```

![29](https://user-images.githubusercontent.com/124214430/228469679-bf0f8fa7-0991-4291-b05f-0bb1cc937e65.png)

The asterisk symbol (*) is used in the select clause to indicate "all attributes." 

```
select name, course id 
from instructor, teaches 
where (instructor.ID, dept name) = (teaches.ID, ’Biology’);
```

### Set Operations 
Ordering of tuples can be performed using the order by clause, and we can specify the sort order using desc for descending order or asc for ascending order. 

```
select course id 
from section 
where semester = ’Fall’ and year= 2009;
```

```
select course id 
from section 
where semester = ’Spring’ and year= 2010;

```

![30](https://user-images.githubusercontent.com/124214430/228469710-78a79466-4af6-4aaf-8040-87dde5c5df00.png)

The between comparison operator can be used to simplify where clauses that specify a value between two values. The SQL operations union, intersect, and except are used for set operations.

```
(select course id 
from section 
where semester = ’Fall’ and year= 2009) 
union
(select course id 
from section 
where semester = ’Spring’ and year= 2010);
```

The union operation eliminates duplicates automatically.

The three set operations in SQL are:

* union
* intersect
* except

```
(select course id 
from section 
where semester = ’Fall’ and year= 2009) 
union all
(select course id 
from section 
where semester = ’Spring’ and year= 2010);
```

```
(select course id 
from section 
where semester = ’Fall’ and year= 2009) 
intersect
(select course id 
from section 
where semester = ’Spring’ and year= 2010);
```

![31](https://user-images.githubusercontent.com/124214430/228469781-8e5655a5-01c3-4c8a-8144-68830573faac.png)

The union operation combines the results of two queries, and it eliminates duplicates by default. However, if we want to retain duplicates, we must use union all instead of union. 

![32](https://user-images.githubusercontent.com/124214430/228469813-2829da6a-a184-4e9b-84e3-af7f8e7106d7.png)

```
(select course id 
from section 
where semester = ’Fall’ and year= 2009) 
intersect all
(select course id 
from section 
where semester = ’Spring’ and year= 2010);
```


The intersect operation finds the common elements between two sets, and it automatically eliminates duplicates. But, if we want to keep duplicates, we must use intersect all instead of intersect. Finally, the except operation finds the difference between two sets, and it automatically eliminates duplicates. 

```
(select course id 
from section 
where semester = ’Fall’ and year= 2009) 
except
(select course id 
from section 
where semester = ’Spring’ and year= 2010);
```

For all three operations, the number of duplicates in the result depends on the occurrence of duplicates in both input sets. The article provides examples to clarify the concepts.

The three set operations in SQL are:

* union
* intersect
* except

```
(select course id 
from section 
where semester = ’Fall’ and year= 2009) 
union all
(select course id 
from section 
where semester = ’Spring’ and year= 2010);
```

```
(select course id 
from section 
where semester = ’Fall’ and year= 2009) 
intersect
(select course id 
from section 
where semester = ’Spring’ and year= 2010);
```

The union operation combines the results of two queries, and it eliminates duplicates by default. However, if we want to retain duplicates, we must use union all instead of union. 

![33](https://user-images.githubusercontent.com/124214430/228469871-767b258f-a4d9-4e92-878e-b79251d96e7f.png)

```
(SELECT course.id
FROM section
WHERE semester = 'Fall' AND year = 2009)
INTERSECT ALL
(SELECT course.id
FROM section
WHERE semester = 'Spring' AND year = 2010);
```


The intersect operation finds the common elements between two sets, and it automatically eliminates duplicates. But, if we want to keep duplicates, we must use intersect all instead of intersect. Finally, the except operation finds the difference between two sets, and it automatically eliminates duplicates. 

```
(select course id 
from section 
where semester = ’Fall’ and year= 2009) 
except
(select course id 
from section 
where semester = ’Spring’ and year= 2010);
```

For all three operations, the number of duplicates in the result depends on the occurrence of duplicates in both input sets. The article provides examples to clarify the concepts.

### Null Values 
In the realm of relational operations, the ubiquitous presence of null values poses unique challenges. Arithmetical expressions involving operators such as +, −, ∗, and / can have their results thrown into disarray when one or more of their input values are null. Consider an expression like r.A+5; if the value of r.A happens to be null for a particular tuple, then the expression's result must also be null for that same tuple.

However, comparisons with nulls can be an even more formidable obstacle. For instance, if we take the comparison “1 < null,” it would be fallacious to assert that it is true since the null value's meaning is unknown. At the same time, it would be erroneous to claim that the expression is false, as that would result in “not (1 < null)” evaluating to true, which defies all sense. To navigate this conundrum, SQL designates the outcome of any comparison involving a null value as unknown, thus introducing a third logical value besides true and false.

```
select name 
from instructor 
where salary is null;
```

When using the select distinct clause, identical tuples must be removed. To accomplish this, SQL treats values of corresponding attributes from two tuples as the same if they are both non-null and equal in value or both null. Therefore, two copies of a tuple such as {(’A’, null), (’A’, null)} are considered identical, even if some of the attributes have null values. By using the distinct clause, only one copy of these identical tuples can be retained. It is important to note that nulls are treated differently in predicates, where a comparison “null=null” yields unknown instead of true. This approach of treating tuples as identical is also employed in the set operations union, intersection, and except.

In short, dealing with null values in relational operations requires careful handling and an understanding of how SQL operates with unknown values.

### Aggregate Functions 
SQL provides a powerful set of tools for querying and manipulating data stored in relational databases. One of the most important features of SQL is its support for aggregate functions, which allow users to perform computations on collections of values and return a single result. The five built-in aggregate functions in SQL are average, minimum, maximum, total, and count, each of which takes a set or multiset of values as input and returns a single value.

```
select avg (salary) 
from instructor 
where dept name= ’Comp. Sci.’;
```

Basic aggregation in SQL involves computing an aggregate function on a set of tuples and returning a single tuple as the result. For example, we can use the AVG function to compute the average salary of instructors in the Computer Science department by writing a SQL query that selects the average salary from the instructor table and restricts the results to instructors in the Computer Science department.

```
select avg (salary) as avg salary 
from instructor 
where dept name= ’Comp. Sci.’;
```

![34](https://user-images.githubusercontent.com/124214430/228469997-5f1e7b1b-9a2d-46b8-adb8-230dc4a74410.png)

In more complex cases, we may need to group the tuples in the input relation into subsets based on the values of one or more attributes, and then compute an aggregate function on each subset. This is accomplished using the GROUP BY clause in SQL. For example, we can use the GROUP BY clause to compute the average salary of instructors in each department by grouping the tuples in the instructor table by department name and then computing the average salary for each group.

```
select count (distinct ID) 
from teaches 
where semester = ’Spring’ and year = 2010;
```

```
select count (*) 
from course;
```

![35](https://user-images.githubusercontent.com/124214430/228470024-20cf3891-ed34-4ccd-ab8b-000cd97da0c3.png)

When using the GROUP BY clause, it is important to ensure that any attribute that appears in the SELECT clause but is not part of the GROUP BY clause is enclosed in an aggregate function, to avoid ambiguity in the query. Similarly, we can use the DISTINCT keyword in the COUNT function to eliminate duplicate values before performing the computation. These powerful features of SQL make it a valuable tool for managing and analyzing large datasets in a variety of contexts.

```
select dept name, avg (salary) as avg salary 
from instructor 
group by dept name;
```

```
select avg (salary) 
from instructor;
```

![36](https://user-images.githubusercontent.com/124214430/228470070-310dd7b6-8ec4-44c0-ae68-f9c50a1a2463.png)

### Nested Subqueries 
Structured Query Language (SQL) provides a powerful mechanism for nesting subqueries, a technique that allows select-from-where expressions to be embedded within other queries. This capability is frequently employed to perform a range of operations, including set membership tests, set comparisons, and set cardinality evaluations. 

One common use of nested subqueries is to test for set membership using the in-connective, which tests whether a given tuple belongs to a relation. This is achieved by constructing a set of values using a select clause and testing for membership using the in operator. Conversely, the not-in operator is used to test for the absence of set membership.

```
select distinct course id 
from section 
where semester = ’Fall’ and year= 2009 and
        course id in (select course id 
            from section 
            where semester = ’Spring’ and year= 2010);
```

SQL’s flexibility enables users to craft queries using different approaches to arrive at the same results. For example, consider the query "Find all the courses taught in both the Fall 2009 and Spring 2010 semesters." The not-in construct is similarly used to test for membership in the absence of a set. The ability to test for membership in arbitrary relations further extends the capabilities of SQL.


```
select distinct course id 
from section 
where semester = ’Fall’ and year= 2009 and
course id not in (select course id 
        from section 
        where semester = ’Spring’ and year= 2010);
```

In summary, the power and flexibility of SQL's nested subqueries enable sophisticated set manipulations and set comparisons, making it a highly valuable tool for data management and analysis.

In the vast realm of data manipulation, SQL provides a powerful tool for the discerning data analyst - the nested subquery. Such a subquery is essentially a select-from-where expression that is nested within another query, and it can be used to perform tests for set membership, make set comparisons and determine set cardinality.

One particularly interesting use of nested subqueries is to test for set membership using the 'in' connective in the where clause. For example, to find all courses taught in both the Fall 2009 and Spring 2010 semesters, we can first find all courses taught in the latter semester using a subquery, and then nest that subquery in the where clause of an outer query to find those courses that were also taught in Fall 2009. The resulting query is both flexible and efficient, allowing the user to approach the problem in a way that seems most natural.

```
select distinct course id 
from section 
where semester = ’Fall’ and year= 2009 and
course id not in (select course id 
        from section 
        where semester = ’Spring’ and year= 2010);
```

Nested subqueries can also be used to compare sets, as in the query "Find the names of all instructors whose salary is greater than at least one instructor in the Biology department." This can be written using the > some construct, which generates the set of all salary values of instructors in the Biology department and compares them to the salary values of the instructors in the outer query.

```
select distinct T.name 
from instructor as T, instructor as S 
where T.salary > S.salary and S.dept name = ’Biology’;
```

```
select name 
from instructor 
where salary > all (select salary 
                    from instructor 
                    where dept name = ’Biology’);
```

SQL offers a wide range of options for testing set membership and comparison using nested subqueries, making it an indispensable tool for data analysts in their quest for insights and knowledge.

In the world of database management, SQL is the lingua franca, enabling users to execute complex queries and sift through mountains of data with ease. But beyond its standard comparison operators, SQL boasts a number of lesser-known, yet equally powerful features that can be harnessed to produce sophisticated results.

```
select dept name 
from instructor 
group by dept name 
having avg (salary) >= all (select avg (salary)
                            from instructor 
                            group by dept name)
```

For instance, by using set comparisons, one can identify departments with the highest average salary, or courses taught in both the Fall 2009 and Spring 2010 semesters. These queries involve the use of subqueries, including correlated subqueries, and scoping rules to ensure that the right data is being accessed.

Additionally, SQL includes features for testing empty relations, checking for duplicate tuples, and testing the absence of duplicate tuples. With the "exists" construct, one can test whether a subquery has any tuples in its result, while the "unique" construct returns true if the argument subquery contains no duplicate tuples.


```
select T.course id 
from course as T 
where unique (select R.course id 
                from section as R 
                where T.course id= R.course id and
                R.year = 2009);
```

By utilizing these advanced features of SQL, users can gain greater insights into their data and extract more value from it. It is a testament to the power and versatility of this programming language that it remains a vital tool in the ever-expanding world of big data.

### Modiﬁcation of the Database 
In the world of database management, the ability to add, remove, or change information is a critical aspect of data processing. While we have thus far focused on information extraction, the manipulation of data is an equally vital function, made possible through the power of SQL.

Deletion is a key operation that can be expressed in a way that is similar to a query, allowing for the removal of entire tuples. It is important to note that only whole tuples can be deleted; values on specific attributes cannot be removed. 

```
delete from r 
where P;
```

The predicate in the "where" clause can be as complex as that of a select command’s "where" clause. The request "delete from instructor" is an example of deleting all tuples from the "instructor" relation. However, the "instructor" relation itself still exists but is emptied of all tuples.

```
delete from instructor 
where dept name in (select dept name 
from department 
where building = ’Watson’);
```

Insertion of data is achieved by either specifying a tuple to be inserted or writing a query that results in a set of tuples to be inserted. In both cases, the attribute values for inserted tuples must be members of the corresponding attribute’s domain, and the tuples inserted must have the correct number of attributes.

```
insert into student 
values (’3003’, ’Green’, ’Finance’, null);
The tuple inserted by this request speciﬁed that a student with ID “3003” is in the Finance department, but the tot cred value for this student is not known. Consider the query:
```

The simplest insert statement involves inserting one tuple, with attribute values specified in the order in which the corresponding attributes are listed in the relation schema.  In more complex cases, we may want to insert tuples on the basis of the result of a query. SQL allows this through the use of the "insert into" statement, followed by a "select" statement that specifies the set of tuples to be inserted. This is particularly useful when inserting data into a relation with a large number of attributes. It is essential to evaluate the "select" statement fully before any insertions are carried out to avoid unexpected results.

```
select student 
from student where tot cred > 45;
```

Deletion and insertion of data are the two most common operations used for modifying a database, and SQL provides a powerful and flexible way to accomplish these tasks. By using SQL, we can add, remove, or change data with ease, allowing us to better manage and analyze vast amounts of information.

```
update instructor 
set salary = salary *1.05 where salary < 70000;
```

SQL, the language of relational databases, offers a versatile set of tools for manipulating data in tables. One of the most frequently used operations is the update statement, which modifies the values of selected tuples in a given relation. To identify which tuples to update, SQL uses a where clause that can include any construct legal in the where clause of a select statement, including nested selects.

In the case of a nested select within an update statement, the relation being updated may be referenced. SQL tests all tuples in the relation to see whether they should be updated and carries out the updates afterward.

As a practical example, consider the request “Give a 5 percent salary raise to instructors whose salary is less than average”. This can be expressed in SQL as an update statement that includes a nested select to calculate the average salary of instructors.

```
update instructor 
set salary = salary *1.05 
where salary < (select avg (salary)
from instructor);

```

```
update instructor 
set salary = salary *1.03 where salary > 100000;
update instructor 
set salary = salary *1.05 where salary <= 100000;
```


In some cases, it may be necessary to perform multiple updates with different criteria. In these situations, SQL provides a case construct that allows for multiple conditions to be evaluated and updated within a single statement. Additionally, scalar subqueries can be useful in the set clause of update statements, allowing for complex calculations to be performed on a per-tuple basis.


Overall, the flexibility and power of SQL's update statement makes it a critical tool for any data professional working with relational databases.

## Intermediate SQL
This chapter delves deeper into SQL, covering complex query forms, view definitions, transactions, integrity constraints, detailed data definition, and authorization.

### Join Expressions
In this section, we delve deeper into join operations in SQL beyond the natural join. The natural join requires matching values across specified attributes, whereas the join operator we examine in this section enables us to specify an explicit join predicate, allowing us to broaden the criteria for matching tuples.

![37](https://user-images.githubusercontent.com/124214430/228470167-c06d0cbb-5a9a-4400-a4f7-b4388927d6df.png)

![38](https://user-images.githubusercontent.com/124214430/228470195-ee5fa05a-45cc-4c5f-9e45-3e79cc410902.png)

We use the student and takes relations, depicted in the Figures displayed above, respectively, to illustrate the examples discussed in this section. Of note is the null value for the grade attribute associated with a student with ID 98988 in the takes relation. This null value indicates that the grade for that course has not been awarded yet.

We begin with the on condition, which is a form of joint that can accommodate a general predicate over the relations being joined. The on condition is written like a where clause predicate, except that the keyword on is used instead of where. As the name implies, the on condition appears at the end of the join expression.

To illustrate, consider the following query that employs the on condition:

```
Copy code
select * 
from student join takes on student.ID= takes.ID;
```

![39](https://user-images.githubusercontent.com/124214430/228470229-579fa092-2460-45f3-a309-f130532bc2fa.png)

The on condition stipulates that a tuple from the student relation matches a tuple from the takes relation if their ID values are equal. The resulting join expression is similar to the student natural join takes operation, except that the ID attribute is listed twice in the join result, once for the student and once for takes. However, the two ID attributes must have the same value.

Interestingly, the preceding query is equivalent to the following one:


```
select * 
from student, takes 
where student.ID= takes.ID;
```

As seen earlier, the relation name is used to disambiguate the attribute name ID, allowing us to refer to the two occurrences as students.ID and takes.ID, respectively. A version of the query that displays the ID value only once is:

```
select student.ID as ID, name, dept name, tot cred, course id, sec id, semester, year, grade 
from student join takes on the student.ID= takes.ID;
```

![40](https://user-images.githubusercontent.com/124214430/228470263-61b913ea-8644-4acc-a85a-9330a3894f56.png)

The query result is depicted in the Figure.

While the on condition allows for more expressive join predicates than the natural join, it may seem redundant since an equivalent expression without the on condition can be written, with the predicate in the on clause moved to the where clause.

### Views
In today's world of data management, it is of utmost importance to ensure that sensitive information is kept secure and out of the reach of unauthorized personnel. In the realm of databases, this can be achieved through the use of views.

Views are virtual relations that can be defined in SQL through the CREATE VIEW command. They allow users to have a customized, personalized collection of relations that is better matched to their needs and intuition than the logical model. For instance, consider a clerk who needs to know an instructor's ID, name, and department, but should not have authorization to view the salary amount. A view relation, such as 'faculty', can be created for the clerk, containing only the necessary attributes.


```
select course.course id, sec id, building, room number from course, section 
where course.course id = section.course id 
and course.dept name = ’Physics’ 
and section.semester = ’Fall’ 
and section.year = ’2009’;
```

Views are not precomputed and stored, but are computed by executing the query whenever the view is used. Thus, the view relation is created whenever needed, on demand. This ensures that the information is always up to date and accurate, as the tuples are generated by computing the query result each time.

```
create view faculty as 
select ID, name, dept name 
from instructor;
```

Furthermore, it is possible to create multiple views on top of any given set of actual relations, allowing for a large number of views to be supported. Using the view name, users can refer to the virtual relation that the view generates and use it in SQL queries.

```
create view departments total salary(dept name, total salary) as select dept name, sum (salary) 
from instructor 
group by dept name;
```

Views in SQL provide a secure and flexible way of accessing and manipulating data, allowing users to have a customized and intuitive collection of relations that are always up to date and accurate.

In the realm of database systems, a compelling technique for querying large volumes of data is through the use of views. These are essentially virtual tables, whose contents are derived from the values of the underlying base relations, but presented to the user in a more intuitive and meaningful manner However, when it comes to modifying the database, the use of views presents serious challenges.

To address the aforementioned challenge, some database systems offer the concept of materialized views. These views not only store the results of the query, but also keep them up-to-date with any changes to the underlying base relations. However, the maintenance of materialized views comes with its own set of concerns, including storage costs and added overhead for updates. Despite these trade-offs, applications that frequently use views, or demand fast response times for large aggregates can benefit greatly from the use of materialized views.

```
create view instructor info as 
select ID, name, building 
from instructor, department 
where instructor.dept name= department.dept name;
```

![41](https://user-images.githubusercontent.com/124214430/228470304-7a05bc4c-a9ae-41e2-b61d-1bbc53df32e3.png)

On the other hand, modifying the database through views is fraught with difficulties. This is because any change to the database expressed in terms of a view must be translated to a modification to the actual relations in the logical model of the database. For instance, the addition of a tuple through a view raises the question of how to assign a value for the salary attribute, given that it is not present in the view. Similarly, the insertion of a tuple through a view with multiple relations may require the use of nulls, which can lead to unexpected and undesired results.

```
insert into instructor info 
values (’69987’, ’White’, ’Taylor’);
```

Given these complexities, most database systems limit the use of updates, insertions or deletions through views, and specify different conditions under which they permit them. The challenge of modifying databases through views has been a subject of considerable research, and further investigation is necessary to determine the most effective solutions.

### Transactions
In the realm of database management, transactions serve as a vital tool to ensure the integrity of data in the face of errors or system failures. A transaction is a series of query and/or update statements, with the SQL standard mandating that the beginning of a transaction is triggered implicitly by the execution of an SQL statement. The completion of a transaction can occur in one of two ways: by committing the transaction via the "commit work" statement, which makes the updates performed by the transaction a permanent part of the database, or by rolling back the transaction via the "rollback work" statement, which undoes all the updates performed in the transaction and restores the database to its previous state.

In this way, transactions can be thought of as atomic operations that are indivisible - either all of the transaction's effects are reflected in the database, or none are. Transactions are especially important in applications such as banking or university management, where the updating of multiple pieces of data must occur simultaneously. If, for example, a power outage occurs after the subtraction of funds from one account in a banking application, but before the addition of funds to another account, the balances will be inconsistent.

It should be noted that some SQL implementations treat each SQL statement as a transaction in its own right, with individual statements being committed as soon as they are executed. To execute a transaction consisting of multiple SQL statements, the automatic commit of individual SQL statements must be turned off. Alternatively, multiple SQL statements can be enclosed between the keywords "begin atomic" and "end", as per the SQL:1999 standard.

While the specifics of implementing transactions may vary depending on the SQL implementation, it is clear that they are an essential tool for ensuring the reliability and consistency of data in complex applications. The intricacies of transactions and their implementation are explored further in later chapters.

### Integrity Constraints
Integrity constraints are vital in ensuring that any changes made to a database do not compromise the system's data consistency. These constraints serve as safeguards against inadvertent damage to the database, which can occur due to various reasons, including human error. Examples of integrity constraints include ensuring that an instructor's name is not null, no two instructors have the same instructor ID, and a department's budget is greater than $0.00.

While an integrity constraint can be any arbitrary predicate pertaining to the database, testing such constraints can be expensive. Therefore, most database systems allow users to specify integrity constraints that can be tested with minimal overhead. These constraints are usually identified during the database schema design process and declared as part of the create table command used to create relations. However, integrity constraints can also be added to an existing relation using the command "alter table table-name add the constraint."

```
name varchar(20) not null
budget numeric(12,2) not null
```

There are several types of integrity constraints that can be included in the create table command, such as not null, unique, and check. The not null constraint, for instance, restricts the domain of certain attributes to exclude null values. This constraint prohibits the insertion of a null value for the attribute and generates an error diagnostic if attempted. Similarly, the unique constraint specifies that no two tuples in the relation can be equal on all the listed attributes, with candidate key attributes allowed to be null unless explicitly declared not null.

```
unique (Aj1, Aj2,..., Ajm)
```

Overall, the use of integrity constraints is crucial in maintaining data consistency in a database system, and their inclusion in the design process can help prevent costly errors and ensure the reliability of the system.

The SQL language provides a variety of mechanisms to ensure data integrity in relational databases, including the check clause and referential integrity constraints. When used in a relation declaration, the check clause allows the specification of a predicate that must be satisfied by every tuple in the relation, effectively creating a powerful type system that restricts attribute domains in ways that most programming-language type systems cannot. For example, a clause such as "check (budget > 0)" would ensure that the value of the budget attribute in a relation called department is nonnegative.

```
create table section
(course id varchar (8), 
sec.id varchar (8), 
semester varchar (6),
year  numeric (4,0),
building varchar (15), 
room number varchar (7), 
time slot id   varchar (4), 
primary key (course id, sec id, semester, year), 
check (semester in (’Fall’, ’Winter’, ’Spring’, ’Summer’)));
```

Referential integrity, on the other hand, ensures that a value appearing in one relation for a given set of attributes also appears for a certain set of attributes in another relation. Foreign keys can be used to specify referential integrity constraints in SQL, with the foreign key clause declaring that for each tuple in a relation, a specified attribute must exist in another relation. The referenced attribute can be a primary key or a candidate key, which is declared using either a primary key or a unique constraint.

```
dept name varchar(20) references department
```

While the SQL standard permits the use of subqueries in the predicate of a check clause, none of the widely used database products currently support this feature. Nonetheless, the check clause and referential integrity constraints are valuable tools for ensuring the correctness and consistency of relational data.

In the realm of relational databases, referential-integrity constraints are a critical element in maintaining consistency and accuracy. These constraints act as guardians, ensuring that any updates or modifications to the database do not result in a violation of the data relationships. Typically, when a referential-integrity constraint is violated, the system's standard response is to reject the action, and the transaction performing the update is rolled back. However, with the use of foreign key clauses, a violation of the constraint can be handled differently.


```
create table classroom
(building varchar (15), 
room number varchar (7), 
capacity numeric (4,0), 
primary key (building, room number))

reate table department
(dept name varchar (20), 
building varchar (15), 
budget numeric (12,2) check (budget >0),
primary key (dept name))

create table course
(course id varchar (8),
title varchar (50), 
dept name varchar (20), 
credits numeric (2,0) check (credits >0), 
primary key (course id), 
foreign key (dept name) references department)

reate table instructor
(ID varchar (5), 
name varchar (20), not null
dept name  varchar (20), 
salary numeric (8,2), check (salary > 29000), 
primary key (ID), 
foreign key (dept name) references department)

reate table section
(course id varchar (8), 
sec id varchar (8), 
semester varchar (6), check (semester in
                                (’Fall’, ’Winter’, ’Spring’, ’Summer’),
year    numeric (4,0), check (year > 1759 and year < 2100) 
building varchar (15), 
room number varchar (7), 
time slot id varchar (4), 
primary key (course id, sec id, semester, year), 
foreign key (course id) references course, 
foreign key (building, room number) references classroom)
```

By including a foreign key clause in the schema, developers can specify that instead of rejecting the action, the system must take measures to restore the constraint. For instance, if a tuple is deleted from the referenced relation, causing a violation of the integrity constraint, the system will not reject the deletion. Instead, if a "delete cascade" clause is included in the foreign-key declaration, the system will propagate the deletion to the referencing tuples in the dependent relation. Similarly, an "update cascade" clause will result in the system updating the referencing tuples to reflect the updated value.

It is worth noting that the use of null values in foreign keys can complicate the application of referential-integrity constraints. While null values are allowed for attributes of foreign keys, the system's response to them may not always be the correct choice. Therefore, SQL provides developers with constructs that allow them to specify alternative behaviors when dealing with null values.

```
create table course
( ... 
foreign key (dept name) references department 
on delete cascade 
on update cascade,
... );
```

Overall, the handling of referential-integrity constraints is a vital component of maintaining data accuracy and consistency. With the proper use of foreign key clauses and a clear understanding of how null values impact the constraints' application, developers can ensure that their relational databases function correctly and reliably.

In the world of databases, maintaining data integrity is of utmost importance. While the SQL standard offers constructs to specify integrity constraints, it must be noted that these constructs are not currently supported by most database systems. However, they can include subqueries in the check clause to verify referential-integrity constraints.

Complex check conditions and assertions can be effective tools to ensure data integrity. Nevertheless, they can be a double-edged sword due to the high cost of testing and maintaining them. Assertions, which express conditions that the database must always satisfy, can be used to articulate constraints that are not expressible using domain constraints or referential-integrity constraints.

When an assertion is created, it undergoes rigorous testing for validity. If valid, future modification to the database is allowed only if it does not violate the assertion. However, this testing can introduce significant overhead when dealing with complex assertions, and thus should be utilized with care.

Despite the limitations of most database systems in supporting sub-queries in the check clause predicate or the create assertion construct, equivalent functionality can still be implemented using triggers. The referential-integrity constraint on time slot ID, for example, can be implemented using triggers.

```
create assertion credits earned constraint check
(not exists (select ID 
from student 
where tot cred <> (select sum(credits) 
from takes natural join course 
where student.ID= takes.ID 
and grade is not null and grade<> ’F’ )
```

The world of databases may be complex, but it is an essential aspect of modern-day life. As such, it is important to remain vigilant when maintaining data integrity and to utilize the most effective tools available to do so.


### SQL Data Types and Schemas
We explored integer types, real types, and character types, and now we shall unravel some of the lesser-known data types supported by SQL, in addition to creating basic user-defined types.

Such a set of data types is the date and time types. These allow for the storage of calendar dates and the time of day in hours, minutes, and seconds. A variant of the time type allows for the specification of fractional digits for seconds, and time zone information can also be stored along with the time.

Another data type is the timestamp, which combines date and time. It too has a variant that allows for the specification of the number of fractional digits for seconds, and time-zone information can be included as well.

```
date ’2001-04-25’ 
time ’09:30:00’ 
timestamp ’2001-04-25 10:29:01.45’
```

To specify a date and time value, one can use the format year followed by month followed by day. A string can be converted to the appropriate data type using the cast expression.

```
reate table student
(ID varchar (5), 
name varchar (20) not null, 
dept name varchar (20), 
tot cred numeric (3,0) 
default 0, primary key (ID));
```

SQL provides several functions to extract individual fields from a date or time value, and it allows comparison operations on all the types listed here. SQL also offers a data type called interval that enables computations based on dates and times.

Furthermore, SQL permits the specification of default values for attributes, as demonstrated by the create table statement. The default value is set to 0 for the tot cred attribute in this example, and this value is assigned when a tuple is inserted into the student relation without a value for the tot cred attribute.

```
insert into student(ID, name, dept name) 
values (’12789’, ’Newman’, ’Comp. Sci.’);
```

In essence, SQL's data types and schemas offer a range of options for the storage and manipulation of data, making it a powerful tool in the hands of those who know how to wield it.

In the world of database management, indexing is a crucial tool for efficient querying. With many queries referencing only a small proportion of records, it's wasteful for the system to scan through every tuple of relation to find the desired results. That's where index creation comes in.

```
Create index studentID index on student(ID);
```

An index is a data structure that allows a database system to efficiently find tuples in a relation that have a specific value for an attribute, without the need to scan through all the tuples. This is achieved by creating an index on the attribute, allowing the system to retrieve the desired tuples directly.

```
book review clob(10KB) 
image blob(10MB) 
movie blob(2GB)
```

In addition to single attribute indices, indices can also be created on a list of attributes, such as a combination of name and department name. While the SQL language does not provide syntax for creating indices, many databases offer support for index creation via SQL statements.

When it comes to storing large objects, such as high-resolution medical images or video clips, SQL provides large-object data types. These data types, known as CLOB and BLOB, allow for the storage of kilobyte to gigabyte-scale attributes.

However, retrieving entire large objects into memory can be impractical or inefficient. Instead, applications often use an SQL query to retrieve a locator for a large object and then manipulate the object using the locator. The locator can be used to fetch the large object in small pieces, much like reading data from a file using a read function call.

SQL provides support for user-defined types, enabling the creation of distinct types to enhance data integrity and prevent programming errors. This form of user-defined data types allows for the creation of unique data types that can be used as attributes of relations such as Dollars and Pounds, which are defined as decimal numbers with 12 total digits, two of which are placed after the decimal point.

```
create type Dollars as numeric(12,2) ﬁnal; 
create type Pounds as numeric(12,2) ﬁnal;
```

By utilizing strong type checking, SQL can identify and prevent programming errors such as assigning a value of type Dollars to a variable of type Pounds, which may be due to a programmer forgetting the differences in currency. Additionally, the use of domains, introduced in SQL-92, can add integrity constraints to an underlying type, such as not null and default values.

```
create table department
dept name   varchar (20), 
building varchar (15), 
budget Dollars);
```

Domains differ from user-defined types in that they can have constraints and default values specified on them, while user-defined types are designed to be used in procedural extensions to SQL where it may not be possible to enforce constraints. Furthermore, values of one domain type can be assigned to values of another domain type as long as the underlying types are compatible, whereas user-defined types are strongly typed.

```
create domain DDollars as numeric(12,2) not null;
```


```
create domain YearlySalary numeric(8,2) 
        constraint salary value test check(value >= 29000.00);
```

```
create domain degree level varchar(10) 
        constraint degree level test 
                check (value in (’Bachelors’, ’Masters’, or ’Doctorate’));
```

SQL's support for user-defined types and domains provides a robust and flexible system for managing complex data structures and enforcing data integrity constraints.

Creating tables with similar schemas as existing tables can prove to be a challenging and time-consuming task for developers. However, SQL offers a useful tool in the form of a "create table-like" extension that can assist in this endeavor. By executing a statement such as "create table temp instructor like the instructor," a new table can be generated with the same schema as an existing one.

```
create table temp instructor like instructor;
```

In addition, developers may find it useful to store the result of a complex query as a new table. The SQL:2003 standard provides a simpler and more efficient technique for this task, enabling the creation of a temporary table containing the results of a query with a single statement. This method can be accomplished by executing a command such as "create table t1 as (select * from instructor where dept name= 'Music') with data."

```
create table t1 as
    (select * 
        from instructor 
        where dept name= ’Music’)
        with data;
```

It is worth noting that some database management systems may utilize slightly different syntax to execute these tasks. Nevertheless, the create table ... as statement bears resemblance to the create view statement in that both rely on queries for their definitions. The main difference is that the contents of a table are set when the table is created, whereas a view's contents always reflect the current query result.

Early file systems stored all files in a single directory, making it difficult to name files uniquely. Similarly, early database systems had a single namespace for all relations, which led to coordination issues. To solve this problem, contemporary database systems provide a three-level hierarchy for naming relations: catalogs, schemas, and SQL objects such as relations and views. Each user has a default catalog and schema, and the combination is unique to the user. Different applications and users can work independently without worrying about name clashes.

```
catalog5.univ schema.course
```

The default catalog and schema are part of an SQL environment that is set up for each connection. We can create and drop schemas by means of create schema and drop schema statements. In most database systems, schemas are created automatically when user accounts are created. The schema name is set to the user account name, and it becomes the default schema for the user account. However, creation and dropping of catalogs is implementation-dependent and not part of the SQL standard.

### Authorization
Amidst the labyrinthine universe of database management, Authorization looms large as a fundamental pillar upon which the entire infrastructure of access control rests. At its core, Authorization governs the granting of privileges to users for accessing, inserting, updating, or deleting data - each of which is deemed a distinct privilege. These authorizations can be bestowed upon a user for a particular part of a database, such as a relation or a view, in combination or exclusively, according to the need of the hour.

However, the database system must ensure that each query or update that is submitted by the user is first checked against the granted authorizations, and if found unauthorized, is promptly rejected. It is not only data authorizations but also schema authorizations that can be granted, providing users with the ability to create, modify or delete relations, amongst other functionalities. Furthermore, a user with some form of authorization can also bestow or revoke privileges to other users as deemed necessary.

Amidst the broad tapestry of Authorization lies the all-encompassing and ultimate authority vested in the hands of the Database Administrator. With a sweeping range of permissions, the Database Administrator is granted the power to create new users, restructure the database, and wield control over the entire infrastructure with utmost finesse, much akin to the authority of a superuser, administrator, or operator for an operating system.

The SQL standard is no stranger to privilege authorization, featuring select, insert, update, and delete privileges as the norm. In a single command, a user can grant all available privileges using the convenient shorthand of 'all privileges'. Whenever a new relation is created, the creator is automatically given all privileges on that relation, providing seamless integration into the system.

Authorization conferral is done through the use of the grant statement in the SQL data-definition language. The basic format of the statement includes a privilege list, a relation or view name, and the intended recipient user or role list. Roles are expounded on further in the subsequent section.

Select authorization is required for the reading of tuples in a relation. For example, granting Amit and Satoshi select authorization on the department relation allows them to read its tuples.

```
grant <privilege list> 
on <relation name or view name>
to <user/role list>;
```

```
grant select on department to Amit, Satoshi;
```



Update authorization on a relation is granted on all attributes of the relation or on only a specific few, determined by the inclusion of the list of attributes in the grant statement. Using the grant statement, a user can give Amit and Satoshi update authorization only on the budget attribute of the department relation.

```
grant update (budget) on department to Amit, Satoshi;
```

Insert authorization permits users to insert tuples into a relation while deleting authorization grants users the ability to remove tuples. The 'public' user designation refers to all present and future users of the system, so granting privileges to the public confers those privileges to all users.

```
revoke <privilege list> 
        on <relation name or view name> from <user/role list>;
```


```
revoke select on department from Amit, Satoshi; 
revoke update (budget) on department from Amit, Satoshi;
```

Although the SQL authorization mechanism allows for the granting of privileges on a relation or attributes of a relation, it does not permit authorizations on specific tuples. In order to revoke an authorization, a user may use the revoke statement, which follows the same basic format as the grant. However, revocation of privileges can become complicated if the user receiving the revocation has granted the same privilege to another user. Further details on this issue are explored in the following section.

The crucial importance of authorizations and access control becomes increasingly clear. In particular, the notion of roles has emerged as a powerful and elegant means of granting privileges to users in a more efficient and secure manner.

In a university setting, for instance, a variety of individuals may require access to various aspects of the database, such as instructors, teaching assistants, students, deans, and department chairs. Rather than having to manually assign authorizations to each individual user, roles can be created that encapsulate these privileges and be granted to users accordingly. This not only simplifies the administrative process but also minimizes the risk of security breaches by allowing for more granular control over who can access what.

Roles can be created and managed using SQL commands, such as the creation of a role with the "Create role" statement or the granting of privileges to a role with the "grant" statement. Moreover, the privileges of a user or role are not limited solely to those explicitly granted to them; they also inherit any privileges granted to roles that have been granted to them, creating a chain of permissions that can be managed and controlled at multiple levels.

```
create role instructor;
        grant select on takes
        to instructor;
                grant dean to Amit; 
        create role dean; 
                grant instructor to dean; 
                grant dean to Satoshi;
```

In short, the use of roles in access control is a versatile and essential tool in the arsenal of any database administrator, one that empowers them to grant and revoke privileges in a more efficient and secure manner.


In the realm of database management, authorization on views is a critical concern, as exemplified by a hypothetical scenario in which a staff member requires access to the salaries of faculty members in the Geology department, but is not authorized to view data pertaining to other departments. To address this issue, a view is created, aptly named "geo instructor", that allows for access to only the necessary data while restricting access to sensitive information. However, before processing any queries, the system must first verify that the user is authorized to access the requested data.

```
create view geo instructor as
    (select * 
        from instructor 
        where dept name = ’Geology’);
```

```
select * 
from geo instructor;
```

It is worth noting that creating a view does not automatically grant the creator all privileges on that view. In fact, the creator only receives privileges that do not exceed their existing authorization. For example, a user cannot be granted update authorization on a view without having update authorization on the underlying relations that were used to define the view. If a view is created on which no authorization can be granted, the system will deny the view creation request.

```
grant references (dept name) on department to Mariano;
grant select on department to Amit with grant option;
```

The creation of functions and procedures, which can contain queries and updates, is also supported by SQL. By default, such functions and procedures inherit all the privileges of their creator, but this can be modified using the "SQL security invoker" clause introduced in SQL:2003. This clause allows for the execution of functions and procedures under the privileges of the user who invokes them, as opposed to the privileges of the creator. This capability facilitates the creation of libraries of functions that can be executed under the same authorization as the invoker, enabling greater flexibility and security in database management.

```
revoke grant option for select on department from Amit;
granted by current role
```

In the world of database management, a primitive authorization mechanism for the database schema is specified by the SQL standard. According to this mechanism, only the schema owner can modify the schema, including the creation or deletion of relations, attributes, and indices. However, users are permitted to declare foreign keys when creating relations, thanks to the SQL references privilege. This privilege is granted on specific attributes, allowing users to restrict deletion and update operations on the referenced relation.

![42](https://user-images.githubusercontent.com/124214430/228470474-181aa18c-3f9a-45f9-87dd-0f987964f2d0.png)

But the ability to create foreign keys can restrict future activity by other users, as illustrated by the department relation example. If a user creates a foreign key referencing the department relation, then it is no longer possible to delete the referenced department without modifying the relation. Therefore, a reference privilege is necessary.

Users who are granted authorization may be allowed to pass on this authorization to other users, but by default, they are not authorized to grant the same privilege to others. To allow this, we use the "with grant option" clause when granting privileges, as shown in the example of granting select privileges on the department to Amit. The creator of an object, such as a relation or a role, holds all privileges on the object, including the privilege to grant privileges to others.

Revoking authorization from a user may cause other users to lose the same privilege, a behavior known as cascading revocation. This can be prevented by using the "restrict" option in the revoke statement. While cascading revocation is often the default behavior, it can be inappropriate in some situations, such as when a user has granted privileges to another user. To avoid confusion and ensure that authorization is properly revoked, SQL ensures that authorization is revoked from both users, even if they have granted the same authorization to each other.

In the complex world of database management, understanding these authorization mechanisms is crucial for maintaining a secure and efficient system.

## Advanced SQL
In Chapters 3 and 4, we presented a comprehensive coverage of the fundamental structure of SQL. However, in this chapter, we delve into the more intricate features of the language. Our attention is drawn toward the pivotal issue of accessing SQL from a general-purpose programming language - an indispensable skill for constructing applications that employ a database to store and retrieve data.

We expound on the notion of procedural code execution within the database, an ingenious mechanism that either extends the SQL language to support procedural actions or enables functions defined in procedural languages to be executed within the database. We describe triggers, an exceptional tool that can automatically initiate designated actions when certain events, such as insertion, deletion, or update of tuples in a specified relation, occur.

Furthermore, we discuss the concept of recursive queries, a highly sophisticated technology that allows a query to reference itself. We also elucidate advanced aggregation features supported by SQL that facilitate complex analytical operations on large datasets. To conclude, we explicate the functionality of online analytic processing (OLAP) systems that enable the interactive analysis of vast datasets.

These advanced features are critical for constructing applications that rely on a database to store and retrieve data. They empower developers to automate actions and analyze massive datasets interactively, cementing SQL's status as a cornerstone of modern data management.


### Accessing SQL From a Programming Language
SQL is a language that affords a potent and declarative means of querying data. As a result, composing SQL queries is usually an effortless endeavor when compared to the task of coding the same queries in a general-purpose programming language. However, it is worth noting that access to a general-purpose programming language is indispensable to a database programmer for two fundamental reasons.

Firstly, there are certain queries that cannot be expressed in SQL, given that the expressive power of SQL falls short of that of a general-purpose language such as C, Java, or Cobol. Consequently, for the purpose of composing such queries, SQL must be embedded within a more powerful language.

Secondly, non-declarative actions such as printing reports, user interactions, or transmission of query results to a graphical user interface cannot be achieved from within SQL. Given that querying or updating data is only one component of an application, other components written in general-purpose programming languages are indispensable. In this light, a means must be developed to fuse SQL with a general-purpose programming language for an integrated application.

Two main approaches to accessing SQL from a general-purpose programming language are Dynamic SQL and Embedded SQL. Dynamic SQL facilitates runtime construction and submission of an SQL query as a character string, while Embedded SQL involves identifying SQL statements at compile time using a preprocessor. The preprocessor submits SQL statements to the database system for precompilation and optimization before replacing the SQL statements in the application program with appropriate code and function calls prior to invoking the programming-language compiler.

One of the primary challenges in integrating SQL with a general-purpose programming language is the mismatch between the ways in which these languages manipulate data. While SQL operates on relations and returns relations as a result, programming languages usually operate on a variable at a time, and those variables correspond to the value of an attribute in a tuple in a relation. Thus, a mechanism must be developed to return the result of a query in a way that the program can handle.

This chapter examines two standards for connecting to an SQL database and performing queries and updates. The first standard is JDBC, an application program interface for the Java language. The second standard, ODBC, is an application program interface originally developed for the C language, but later extended to other languages such as C++, C#, and Visual Basic.

The Java Database Connectivity (JDBC) standard is an important tool that enables Java programs to connect with database servers. By providing an application programming interface (API), JDBC allows Java developers to take advantage of database functionality while writing Java code. The API provides a range of capabilities, including opening and closing connections, executing statements, and processing results.

Figure 5.1 provides a clear example of how the JDBC interface works in practice. The example Java program illustrates the process of opening connections, executing statements, and processing results, and it provides a useful framework for developers who are new to the JDBC standard. This section explores the program in detail, providing valuable insights into how JDBC can be used to enhance Java applications.

In order to use JDBC, developers must first import java.sql.* package, which contains the interface definitions for JDBC functionality. Once this is done, the JDBC API can be used to execute SQL queries and interact with databases in a seamless and efficient manner. With its powerful functionality and ease of use, JDBC has become an essential tool for Java developers who need to work with databases.

```
{
        try
        {
                Class.forName ("oracle.jdbc.driver.OracleDriver"); Connection conn = DriverManager.getConnection("jdbc:oracle:thin:@db.yale.edu:1521:univdb", userid, passwd);
                Statement stmt = conn.createStatement(); 
                try { stmt.executeUpdate(
                "insert into instructor values(’77987’, ’Kim’, ’Physics’, 98000)");
                } catch (SQLException sqle) {
                        System.out.println("Could not insert tuple. " + sqle);
                }
                ResultSet rset = stmt.executeQuery( 
                        "select dept name, avg (salary) "+ " from instructor "+
                        " group by dept name");
                while (rset.next()) {
                        System.out.println(rset.getString("dept name") + " " + rset.getFloat(2));
                }
                stmt.close(); 
                conn.close();
        }
        catch (Exception sqle)
        {
                System.out.println("Exception : " + sqle);
        }
}
```      

Opening a connection to a database from a Java program is a crucial first step in the process of executing SQL statements. It requires a careful selection of the database to use, which can be an instance of Oracle running on a local machine or a PostgreSQL database running on a remote one. This initial connection is established using the getConnection method of the DriverManager class, which takes three crucial parameters.

The first parameter specifies the URL or machine name of the server, along with some additional information, including the communication protocol and port number. However, the actual protocol used to exchange information with the database is not defined by the JDBC standard and may vary depending on the driver being used.

To access the database from Java, the JDBC driver must be loaded first, which is achieved by invoking Class.forName with a concrete class implementing the java.sql.Driver interface. It is important to note that each database product that supports JDBC provides its own JDBC driver, which must be dynamically loaded before connecting to the database.

The second and third parameters of the getConnection method require a database user identifier and password, respectively. However, the need to specify a password within the JDBC code presents a significant security risk, particularly if an unauthorized person gains access to the Java code.

Therefore, the process of establishing a connection to a database from a Java program requires a meticulous approach and attention to detail. By carefully selecting the appropriate database and driver, and taking the necessary security precautions, developers can ensure that their Java programs execute SQL statements smoothly and securely.

Once a connection to the database is established, the Java program gains the ability to send SQL statements for execution to the database system. To achieve this, the program makes use of an instance of the Statement class. It's worth noting that the Statement object is not the SQL statement itself, but rather an interface that facilitates the invocation of methods that execute SQL statements.

In the example provided, a Statement handle (stmt) is created on the connection (conn), providing the program with the necessary means to execute SQL statements. To execute a statement, the program uses either the executeQuery method or the executeUpdate method, depending on the nature of the SQL statement. If the statement is a query statement that returns a result set, the executeQuery method is used. Conversely, non-query statements, such as update, insert, delete, create a table, etc., are executed using the executeUpdate method.

The given example employs the stmt.executeUpdate method to execute an update statement that inserts data into the instructor relation. This method returns an integer value that corresponds to the number of tuples inserted, updated, or deleted. DDL statements, however, produce a return value of zero.

To address any exceptions that may arise during JDBC calls, the program employs a try-catch construct. This enables the program to handle any errors and communicate appropriate messages to the user.

By leveraging Statement objects and the appropriate execute methods, Java programs can effectively execute SQL statements and interact with a database system with ease.

Retrieving the result of a query is a critical aspect of data processing. The process involves executing a query and fetching the resulting set of tuples into a ResultSet object, which is then accessed one tuple at a time. In the Java programming language, this is done using the executeQuery method on a Statement object.

The ResultSet object provides a range of methods for fetching attributes from the fetched tuple, including getString and getFloat. These methods can be invoked using either the attribute name or the position of the desired attribute within the tuple.

However, it is crucial to close the connection and statement objects at the end of the program to avoid exceeding the limit of connections imposed on the database. Failure to do so may prevent the application from opening any more connections, disrupting the data processing pipeline.

```
PreparedStatement pStmt = conn.prepareStatement( "
                insert into instructor values(?,?,?,?)");
        pStmt.setString(1, "88877"); 
        pStmt.setString(2, "Perry"); 
        pStmt.setString(3, "Finance"); 
        pStmt.setInt(4, 125000); 
        pStmt.executeUpdate(); 
        pStmt.setString(1, "88878"); 
        pStmt.executeUpdate();
```

To execute a prepared statement, which is a SQL statement with one or more parameters, the program can use an instance of the class PreparedStatement. In the example provided, a PreparedStatement object is created and used to insert tuples into the instructor relation. The setString and setInt methods are used to set the parameter values before executing the update using the executeUpdate method.

Retrieving the result of a query is a critical aspect of data processing. The process involves executing a query and fetching the resulting set of tuples into a ResultSet object, which is then accessed one tuple at a time. In the Java programming language, this is done using the executeQuery method on a Statement object.

The ResultSet object provides a range of methods for fetching attributes from the fetched tuple, including getString and getFloat. These methods can be invoked using either the attribute name or the position of the desired attribute within the tuple.

However, it is crucial to close the connection and statement objects at the end of the program to avoid exceeding the limit of connections imposed on the database. Failure to do so may prevent the application from opening any more connections, disrupting the data processing pipeline.

```
select * from instructor where name = ’X\’ or \’Y\’ = \’Y’
```
To execute a prepared statement, which is a SQL statement with one or more parameters, the program can use an instance of the class PreparedStatement. In the example provided, a PreparedStatement object is created and used to insert tuples into the instructor relation. The setString and setInt methods are used to set the parameter values before executing the update using the executeUpdate method.

Java Database Connectivity (JDBC) provides a robust and flexible way to connect Java applications to databases. One notable feature of JDBC is the CallableStatement interface, which enables the invocation of SQL-stored procedures and functions. CallableStatement, similar to PreparedStatement for queries, allows for the use of functions and procedures in Java applications. By registering out parameters with the registerOutParameter() method, we can retrieve the data types of function return values and procedure out parameters with the get methods. This functionality provides Java applications with an easy way to interact with databases using stored procedures and functions.


```
ResultSetMetaData rsmd = rs.getMetaData(); 
        for(int i = 1; i <= rsmd.getColumnCount(); i++) {
                System.out.println(rsmd.getColumnName(i)); 
                System.out.println(rsmd.getColumnTypeName(i));
}
```

Furthermore, JDBC's metadata features provide Java programs with the means to retrieve metadata about the database at runtime. This approach makes Java applications more robust to changes in the database schema. The ResultSet interface's getMetaData() method returns a ResultSetMetaData object containing metadata about the result set, which includes information such as the number of columns and the name and type of each column. The DatabaseMetaData interface provides even more metadata about the database system, allowing Java applications to obtain information such as product names, version numbers, and supported features.

```
DatabaseMetaData dbmd = conn.getMetaData();
        ResultSet rs = dbmd.getColumns(null, "univdb", "department", "%"); 
        // Arguments to getColumns: Catalog, Schema-pattern, Table-pattern, 
        // and Column-Pattern
        // Returns: One row for each column; row has a number of attributes 
        // such as COLUMN NAME, TYPE NAME 
        while( rs.next()) {
                System.out.println(rs.getString("COLUMN NAME"), rs.getString("TYPE NAME"));
        }
```

The metadata interfaces can be leveraged for a wide range of tasks, such as writing a database browser or generic code to display rows in a relation. Additionally, JDBC provides many other useful features, such as updatable result sets and transaction handling. By utilizing JDBC, Java developers can seamlessly integrate databases into their applications and take full advantage of their capabilities.

In a world where data reigns supreme, accessing and manipulating vast amounts of information is a task of paramount importance. To this end, the Open Database Connectivity (ODBC) standard provides a vital tool for applications seeking to open a connection with a database, send queries and updates, and retrieve results. It is a veritable lifeline for a vast array of applications, from graphical user interfaces to statistics packages to spreadsheets.

Each database system supporting ODBC provides a library that must be linked with the client program. In this way, ODBC acts as a bridge between client and server, facilitating the smooth and efficient communication of information. The ODBC API provides a range of functions for tasks such as finding all the relations in the database and finding the names and types of columns of a query result or a relation in the database.

But what does it look like in practice? The program first allocates an SQL environment and then a database connection handle, using ODBC-defined types such as HENV, HDBC, and RETCODE. From there, the program opens the database connection by calling SQLConnect, passing parameters such as the connection handle, the server to which to connect, the user identifier, and the password for the database.

```
void ODBCexample() 
{
        RETCODE error;
        HENV env; /* environment */
        HDBC conn; /* database connection */

        SQLAllocEnv(&env);
        SQLAllocConnect(env, &conn);
        SQLConnect(conn, "db.yale.edu", SQL NTS, "avi", SQL NTS, "avipasswd", SQL NTS);
        {
                char deptname[80];
                ﬂoat salary; 
                int lenOut1, lenOut2;
                HSTMT stmt; 
                char * sqlquery = "select dept name, sum (salary)
                                from instructor 
                                group by dept name";
               SQLAllocStmt(conn, &stmt); 
                        error = SQLExecDirect(stmt, sqlquery, SQL NTS); 
                        if (error == SQL SUCCESS) 
                {
                SQLBindCol(stmt, 1, SQL C CHAR, deptname , 80, &lenOut1); 
                        SQLBindCol(stmt, 2, SQL C FLOAT, &salary, 0 , &lenOut2); 
                        while (SQLFetch(stmt) == SQL SUCCESS) 
                {
                printf (" %s %g\n", depthname, salary); 
                }
        }
        SQLFreeStmt(stmt, SQL DROP);
        }
        SQLDisconnect(conn);
        SQLFreeConnect(conn); 
        SQLFreeEnv(env); 
}
```

Once the connection is established, SQL commands can be sent to the database via SQLExecDirect, with C language variables bound to attributes of the query result. SQLBindCol facilitates this task, with the second argument identifying the position of the attribute in the query result and the third indicating the type conversion required from SQL to C. On each fetch, SQLFetch retrieves the next result tuple, with attribute values stored in corresponding C variables. The program then prints out these values.

A good programming style requires that the result of every function call be checked for errors. At the end of the session, the program frees the statement handle, disconnects from the database, and frees up the connection and SQL environment handles.

Through ODBC, applications gain the power to communicate with any database server that supports the ODBC standard, providing a level of flexibility and versatility that is vital in today's data-driven landscape.

Embedded SQL is a powerful tool for accessing and manipulating database systems. The SQL standard defines a variety of programming languages in which SQL queries can be embedded, including C, C++, Cobol, Pascal, Java, PL/I, and Fortran. The language in which SQL queries are embedded is known as the host language, and the SQL structures permitted in the host language constitute embedded SQL.

```
EXEC SQL <embedded SQL statement >;
```

To use embedded SQL, a program must be processed by a preprocessor prior to compilation. This preprocessor replaces embedded SQL requests with host-language declarations and procedure calls that allow for runtime execution of database accesses. Unlike JDBC or ODBC, where SQL statements are interpreted at runtime, some SQL-related errors can be caught at compile time when using embedded SQL.

The EXEC SQL statement is used to identify embedded SQL requests to the preprocessor, and the SQL INCLUDE SQLCA statement is used to identify the place where the preprocessor should insert special variables used for communication between the program and the database system. Before executing any SQL statements, the program must connect to the database using the EXEC SQL and connect to the server using a username using a password statement.

```
EXEC SQL BEGIN DECLARE SECTION;
int credit amount;
EXEC SQL END DECLARE SECTION;
```

Variables of the host language can be used within embedded SQL statements but must be preceded by a colon (:) to distinguish them from SQL variables. Embedded SQL statements are similar in form to regular SQL statements but have several important differences. To write a relational query, we use the declare cursor statement, which creates a cursor for the query. The program must use the open and fetch statements to obtain the result tuples.

```
EXEC SQL 
        declare c cursor for 
        select ID, name 
        from student 
        where tot cred > :credit amount;
```

A single fetch request returns only one tuple, so the program must contain a loop to iterate over all tuples. Embedded SQL assists the programmer in managing this iteration, as the cursor is set to point to the first tuple of the result when the program executes an open statement on a cursor. Each time it executes a fetch statement, the cursor is updated to point to the next tuple of the result. The close statement is used to tell the database system to delete the temporary relation that held the result of the query.

Embedded SQL expressions for database modification do not return a result and are somewhat simpler to express. A database modification request takes the form EXEC SQL . Overall, embedded SQL is a powerful tool for accessing and manipulating database systems, and its use can improve the efficiency and reliability of database operations.

```
EXEC SQL < any valid update, insert, or delete>;
```

### Functions and Procedures
While the language comes with a number of pre-built functions, developers can also create their own specialized functions and procedures, store them in the database, and call them from SQL statements. With these custom functions, developers can add business logic to their databases, such as rules for how many courses a student can take in a given semester or how many majors they can be enrolled in.

But the benefits of custom functions don't stop there. Functions can also be used with specialized data types, such as images and geometric objects, where they can perform tasks like checking whether two line segments overlap or comparing two images for similarity. And by storing these functions within the database, developers can ensure that multiple applications have access to them and can change the business rules in one central location without needing to modify other parts of their application.

```
create function dept count(dept name varchar(20))
        returns integer 
        begin 
        declare d count integer;
                select count(*) into d count 
                from instructor 
                where instructor.dept name= dept name 
        return d count; 
        end
```

SQL supports the creation of functions, procedures, and methods, which can be defined using either the procedural component of SQL or an external programming language like Java, C, or C++. And while different database systems may implement these syntaxes in slightly different ways, the concepts we've discussed remain relevant across implementations. So whether you're using Oracle, Microsoft SQL Server, or PostgreSQL, the power of custom functions and procedures is within your reach.

In the realm of the structured query language (SQL), the power of programming language constructs is readily available. To explore this domain, one must delve into the Persistent Storage Module (PSM) - a part of the SQL standard that outlines the language constructs available for writing procedures and functions.

SQL functions in particular, are discussed in detail. For example, define a function that, given the name of a department, returns the count of instructors in that department.

```
create function instructors of (dept name varchar(20)) returns table (
        ID varchar (5), 
                name varchar (20), dept name varchar (20), salary numeric (8,2))
                return table
                (select ID, name, dept name, salary 
                from instructor 
                where instructor.dept name = instructor of.dept name);
```

Variables are declared using a declare statement, and SQL's support for almost all conditional statements makes it an extremely flexible language. From while statements to repeat statements and conditional statements like if-then-else, SQL's flexibility is unparalleled.

```
        if boolean expression 
                then statement or compound statement 
        elseif boolean expression 
                then statement or compound statement 
        else statement or compound statement 
        end if
```

In summary, SQL's PSM provides an incredible suite of tools that give it the power of a general-purpose programming language. With its support for functions and procedures, SQL provides great flexibility in developing applications. Its vast range of language constructs allows developers to write complex code that can handle almost any scenario.

SQL allows for functions to be defined in languages like Java, C#, C, or C++. These functions can be more efficient than SQL-defined functions and can perform computations that SQL cannot. However, external language procedures and functions must handle null values in parameters and return values, communicate failure/success status, and deal with exceptions. The exact mechanisms for handling these situations depend on the database system used.

```
create procedure dept count proc( in dept name varchar(20), 
                                        out count integer)
language C 
external name ’/usr/avi/bin/dept count proc’

create function dept count (dept name varchar(20)) returns integer 
language C 
external name ’/usr/avi/bin/dept count’
```

Although functions defined in programming languages and compiled outside the database system can be loaded and executed with the database-system code, this method carries significant risk. A bug in the program can corrupt the database's internal structures and bypass the access-control functionality of the database system. Some database systems execute procedures in this fashion, prioritizing efficiency over security. However, others execute such code as part of a separate process, communicate the parameter values to it, and fetch results back via interprocess communication. This method incurs a high time overhead, as tens to hundreds of thousands of instructions can execute in the time taken for one interprocess communication.

Alternatively, if the code is written in a "safe" language such as Java or C#, it can be executed in a sandbox within the database query execution process itself. The sandbox allows the Java or C# code to access its memory area while preventing it from reading or updating the memory of the query execution process or accessing files in the file system. This method greatly reduces function call overhead by avoiding interprocess communication.

Today, several database systems support external language routines running in a sandbox within the query execution process, such as Oracle and IBM DB2, which allow Java functions to run as part of the database process. Microsoft SQL Server allows procedures compiled into the Common Language Runtime (CLR) to execute within the database process, written in languages like C# or Visual Basic. PostgreSQL also allows functions defined in several languages, including Perl, Python, and Tcl. The use of external language routines offers a promising solution to the challenges posed by the lack of standardization in procedural extensions to SQL.

### Triggers 
Triggers are powerful mechanisms that can automatically execute certain actions in response to a modification of the database. To design a trigger mechanism, one must specify the trigger event and the conditions for execution, as well as the actions to be taken when the trigger fires. Once implemented, the database system assumes responsibility for executing the trigger whenever the specified event occurs and the conditions are met.

Triggers are often utilized to enforce integrity constraints that cannot be expressed using standard SQL constraints. Additionally, they can serve as valuable tools for automating tasks or alerting humans when certain conditions are met. Take for example a scenario where a student is enrolled in a course - a trigger can be designed to update the student's total credits whenever a new tuple is inserted into the "takes" relation. Similarly, a warehouse may use a trigger to automatically place an order when the inventory level of an item falls below the minimum level.

However, it's important to note that trigger systems are limited in their ability to perform updates outside of the database. Therefore, in the aforementioned warehouse example, a separate process must be created to periodically scan the "reorders" relation and place orders as needed. Some database systems do offer built-in support for sending emails from SQL queries and triggers, but the above approach remains the most common solution.

As we delve into the implementation of triggers in SQL, we are presented with a syntax that is recognized as standard, but the reality is that most databases utilize nonstandard versions of this syntax. Though the syntax we examine may not be upheld on such systems, the underlying concepts are universally applicable. In this regard, it is necessary to consider nonstandard trigger implementations, which we will discuss in greater detail later on in this section.

```
create trigger timeslot check1 after insert on section 
referencing new row as nrow 
for each row 
when (nrow.time slot id not in ( 
        select time slot id 
        from time slot)) /* time slot id not present in time slot */

begin 
        rollback 
end;

create trigger timeslot check2 after delete on timeslot 
referencing old row as orow 
for each row 
when (orow.time slot id not in ( 
                select time slot id 
                from time slot)/*lasttuple for time slot id deleted from time slot */
        and orow.time slot id in ( 
        select time slot id 
        from section)) /* and time slot id still referenced from section*/
begin 
        rollback 
end;

```


To illustrate the efficacy of triggers in enforcing referential integrity on the time slot id attribute of the section relation. The first trigger definition is initiated after any insert on the relation section, and it verifies that the time slot id value being inserted is valid.  The referencing new row as clause establishes a transition variable called nrow, which retains the value of an inserted row after the insertion.

Furthermore, the when statement specifies a condition. Consequently, the system executes the remainder of the trigger body solely for tuples that satisfy the condition. The begin atomic...end clause is employed to collect several SQL statements into a single compound statement. However, in the given example, only one statement is included, which rolls back the transaction that caused the trigger to be executed. In this manner, any transaction that breaches the referential integrity constraint is automatically rolled back, ensuring that the data in the database satisfies the constraint.

```
create trigger reorder after update of amount on inventory 
        referencing old row as orow, new row as nrow 
        for each row 
                when nrow.level <= (select level 
                from minlevel 
                where minlevel.item = orow.item)
        and orow.level > (select level 
                from minlevel 
                where minlevel.item = orow.item)
        begin atomic 
                insert into orders
                (select item, amount 
                from reorder 
                where reorder.item = orow.item);
        end;
```

The trigger is only executed when the grade attribute is updated from a value that is either null or 'F', to a grade that indicates successful completion of the course. The update statement is normal SQL syntax, except for the use of the variable nrow.

Triggers can be less efficient and less transparent than other techniques, and can even create unintended complications.

One example of a better alternative to triggers is the use of materialized views, which many modern database systems support. By contrast, triggers would require writing complex code to maintain the view, which could make it difficult for a database user to understand the constraints in the database. Similarly, while triggers can be used to maintain replicas of databases, built-in facilities for replication are now widely available, which often make triggers unnecessary.


```
select course id, sec id, semester, year, count(ID) as total students 
from takes 
group by course id, sec id, semester, year;
```

In addition to these issues, triggers can also cause problems when loading data from backup copies or replicating database updates on backup sites. In such cases, triggers may execute the triggered action more than once, which can lead to an infinite chain of triggering. As a result, database systems may limit the length of such chains or flag them as an error.

Despite these challenges, triggers remain a useful tool in many cases. However, they should be written with great care to avoid errors and complications. When possible, alternative techniques such as stored procedures should be considered instead. Ultimately, the choice of whether or not to use triggers depends on the specific needs and circumstances of the database in question.

![43](https://user-images.githubusercontent.com/124214430/228470686-6953c7a5-f98b-4d02-aca2-59014977ce32.png)

### Recursive Queries** 
"findAllPrereqs(cid)" take the course id of the course as a parameter (cid), computes the set of all direct and indirect prerequisites of that course, and returns the set. The function uses three temporary tables: c_prereq, new_c_prereq, and temp. The repeat loop then adds all courses in the new_c_prereq table to the c_prereq table. Next, it computes the prerequisites of all those courses in new_c_prereq, except those that have already been found to be prerequisites of cid, and stores them in the temporary table temp. Finally, it replaces the contents of new_c_prereq by the contents of temp. The repeat loop continues until it finds no new (indirect) prerequisites.

It is worth noting that the use of the except clause in the function ensures that the function works even in the (abnormal) case where there is a cycle of prerequisites. This is particularly useful as cycles are possible in other applications. For example, in relation to "flights(to, from)" which says which cities can be reached from which other cities by a direct flight, the function can be adapted to find all cities that are reachable by a sequence of one or more flights.

```
create function ﬁndAllPrereqs(cid varchar(8))
        – – Finds all courses that are prerequisite (directly or indirectly) for
returns table (course id varchar(8))
––The relation prereq(course id, prereq id) speciﬁes which course is
– – directly a prerequisite for another course.
begin 

create temporary table c prereq (course id varchar(8));
        ––table c prereq stores the set of courses to be returned 
create temporary table new c prereq (course id varchar(8));
        ––table new c prereq contains courses found in the previous iteration
create temporary table temp (course id varchar(8));
        ––table temp is used to store intermediate results 
insert into new c prereq 
                select prereq id 
                from prereq 
                where course id = cid;
        repeat 
                insert into c prereq 
                        select course id 
                        from new c prereq;
                insert into temp
                        (select prereq.course id 
                                from new c prereq, prereq 
                                where new c prereq.course id = prereq.prereq id 
                        ) 
                except ( 
                        select course id 
                        from c prereq
                        );
                delete from new c prereq; 
                insert into new c prereq 
                        select * 
                        from temp;
                delete from temp;
        until not exists (select * from new c prereq) end repeat; 
        return table c prereq;
end
```

Overall, this innovative approach to computing the transitive closure of the relation "prereq" has significant implications for a wide range of hierarchical structures, including organizations and machines, where transitive closure can be used to find all parts in a system.

![44](https://user-images.githubusercontent.com/124214430/228470752-2a6d4630-a3f8-4821-bbad-25aa75dae6a0.png)

Using recursion in SQL, we can, for example, define the set of courses that are prerequisites for a particular course by recursively identifying courses that are prerequisites for other courses, until we arrive at the desired course. This approach can be expressed using the "with recursive" clause.

```
with recursive c prereq(course id, prereq id) as ( 
                select course id, prereq id 
                from prereq 
        union 
        select prereq.prereq id, c prereq.course id from prereq, c prereq 
        where prereq.course id = c prereq.prereq id 
        )
select ∗ 
from c prereq;
```

However, there are certain constraints to be aware of when constructing a recursive view. The recursive query must be monotonic, meaning that if more tuples are added to the view relation, the recursive query should return at least the same set of tuples as before, and possibly return additional tuples. Constructs such as aggregation do not exist in subqueries, and the set differences can cause the query to be nonmonotonic and should therefore be avoided.

Despite these constraints, recursive views remain a valuable tool in the database programmer's arsenal, providing a powerful means of expressing transitive closure with ease and efficiency. By applying an iterative procedure, we can compute a fixed point instance of the view relation, containing exactly the tuples necessary for expressing the desired transitive closure. So the next time you find yourself struggling with transitive closure in SQL, remember the power of recursion and the convenience of recursive view definitions.

### Advanced Aggregation Features**
In the field of database management, aggregation support in SQL is a powerful tool that can tackle most common tasks with ease. However, there are some complex tasks that prove to be difficult to implement efficiently with the basic aggregation features. This is where the ingenious additions to SQL come into play.

In this section, we explore the ranking feature added to SQL that enables users to find the position of a value in a larger set, a common operation in data analysis. For instance, in the academic world, professors may wish to rank their students based on their grade-point average (GPA). The rank 1 goes to the student with the highest GPA, the rank 2 to the student with the next highest GPA, and so on. SQL's ranking feature allows users to accomplish this task with ease.

In addition to finding the rank, users can also find the percentile in which a value in a (multi)set belongs. While SQL's basic constructs can express such queries, they are often difficult to execute and inefficient. Programmers may resort to writing the query partly in SQL and partly in a programming language.

To illustrate the use of ranking in SQL, we can examine the example of a university's student grades (ID, GPA) view. The following query uses the rank function to give the rank of each student based on their GPA:

```
select ID, rank() over (order by (GPA) desc) as s rank 
from student grades;
```

It is important to note that the order of tuples in the output is not defined, so they may not be sorted by rank. An extra order by clause is required to get them in sorted order. The rank function gives the same rank to all tuples that are equal on the order by attributes. In contrast, the dense rank function does not create gaps in the ordering. It assigns the same rank to tuples with the same GPA and increments the rank for the next unique GPA value.

Ranking can also be performed within partitions of the data. For example, if we want to rank students by department rather than across the entire university, we can use the partition by clause. The following query gives the rank of students within each department:

```
select ID, dept name, 
        rank () over (partition by dept name order by GPA desc) as dept rank 
from dept grades 
order by dept name, dept rank;
```

Multiple rank expressions can be used within a single select statement. Moreover, when ranking (possibly with partitioning) occurs along with a group by clause, the group by clause is applied first, and partitioning and ranking are done on the results of the group by. This allows users to obtain aggregate values that can then be used for ranking.

While SQL's ranking functions can be used to find the top n tuples by embedding a ranking query within an outer-level query, several database systems provide nonstandard SQL extensions that simplify the job of the optimizer. For instance, some databases allow a clause limit n to be added at the end of an SQL query to specify that only the first n tuples should be output.

SQL's ranking feature is an innovative addition to its suite of tools that offers users a simple and efficient way to perform complex tasks. By leveraging SQL's ranking functions, users can easily rank their data based on various criteria, making data analysis a breeze.

The concept of windowing in databases is a powerful tool for computing aggregate functions over ranges of tuples. By specifying a window, which may overlap with other windows, one can compute aggregate values for specific time intervals, as well as analyze trends in various data sets.

One practical use of windowing is in trend analysis, such as analyzing sales figures or stock market trends. While it is relatively straightforward to compute aggregates over a fixed window of time, such as a 3-day period, it becomes more challenging to do so for every 3-day period. This is where the windowing feature of SQL comes in handy.


```
select year, avg(num credits) 
        over (order by year rows 3 preceding) 
        as avg total credits 
from tot credits;
```

SQL allows for the computation of aggregate values over specific windows by using the "rows preceding" or "rows following" syntax. For example, a query could be written to compute the average number of credits taken by students over the previous three years, sorted by year. Additionally, the "range between" syntax can be used to specify a range based on the value of the order attribute.

```
select year, avg(num credits) 
        over (order by year rows unbounded preceding) 
        as avg total credits 
from tot credits;

```

```
select year, avg(num credits) 
        over (order by year rows between 3 preceding and 2 following) 
        as avg total credits 
from tot credits;
```

Furthermore, windowing can be used to partition data by specific attributes, such as department names, in order to compute aggregate values for each subset of data. This is done by including a "partition by" clause in the SQL query.

```
select dept name, year, avg(num credits) 
        over (partition by dept name 
                order by year rows between 3 preceding and current row)
        as avg total credits 
from tot credits dept;
```

Overall, the windowing feature in SQL provides a powerful tool for analyzing trends and computing aggregate values over specific windows of data. Its flexibility and ease of use make it an essential tool for data analysis and decision-making in a wide variety of fields.

### OLAP**
The art of data analysis has come a long way since the days of spreadsheet applications. In today's world, businesses are looking for more sophisticated ways to make sense of their vast amounts of data. Enter the online analytical processing (OLAP) system, a revolutionary tool that allows analysts to view summaries of multidimensional data in an interactive and speedy fashion.

```
sales (item name, color, clothes size, quantity)
```

![45](https://user-images.githubusercontent.com/124214430/228470833-12eef1cb-8e33-4c9c-aa4d-2549939469b7.png)

OLAP systems are available in many forms, including those that come bundled with database products like Microsoft SQL Server and Oracle, as well as standalone tools. While spreadsheet applications can handle smaller amounts of data, OLAP systems are necessary for larger datasets that require efficient preprocessing and online query processing support from databases.

To better understand the power of OLAP, let's consider a hypothetical scenario. A clothing store wants to know what types of clothes are popular among their customers. By using a sales relation with attributes such as item name, color, and clothes size, managers can group their data and view summaries in a cross-tabulation (or pivot table) format. The table shows total quantities for different combinations of item name and color, with clothes size being a summary across all values.

Multidimensional data, with measure and dimension attributes, is essential for this type of analysis. OLAP systems allow managers to quickly group and view data in a cross-tabulation format, providing valuable insights for business decisions. By extending SQL to support these tasks, OLAP systems are at the forefront of data analysis technology.

![46](https://user-images.githubusercontent.com/124214430/228470866-5b546bba-a98e-48d6-83dd-68a37d4ae16e.png)

![47](https://user-images.githubusercontent.com/124214430/228470886-fc068a4c-fab4-45c8-835f-634f954b882c.png)

In the world of data analysis, the use of cross-tabs has become ubiquitous. These tables, which summarize data by showing the intersection of two attributes, are a simple and powerful tool for understanding complex data sets. Most cross-tabs include summary rows and columns, which provide totals for the cells in each row or column.

But what happens when a data set has more than two attributes? Enter the data cube, a multi-dimensional version of the cross-tab that can be visualized as an n-dimensional cube. Each cell in the data cube contains a value, just like a cross-tab, but now the cell is identified by values for multiple dimensions.

The number of different ways to group tuples for aggregation can be vast. For instance, a table with three dimensions for item name, color, and clothes size results in a cube with a size of 3 x 4 x 3 = 36. Including summary values, the cube is 4 x 5 x 4 with a size of 80. Aggregation can be performed with grouping on each of the 2n subsets of the n dimensions.

OLAP systems take the concept of the data cube to the next level, allowing data analysts to interactively select attributes for their cross-tabs. Analysts can pivot their views to create two-dimensional cross-tabs on different attributes or slice the data to view a single value across multiple dimensions.

Drilling up and down hierarchies allows analysts to view data at different levels of granularity, which can be organized into a hierarchy. For example, the hierarchy of location can go from city to state to country to region, while clothing items can be grouped into categories like menswear or womenswear.

The beauty of OLAP systems is the ability to view data at any level of granularity, from fine-grained data to coarser-grained data. With the power of these tools, data analysts can gain insights and understanding from even the most complex of data sets.

![48](https://user-images.githubusercontent.com/124214430/228470932-7e9fa95a-7db3-480f-a077-f4e4ef3a1ed2.png)

In the realm of database management and online analytical processing (OLAP), the intricacies of cross-tab and relational tables have been a topic of much discussion. A cross-tab, in particular, is an entity that differs from the typical relational tables stored in databases, as its columns are contingent on the data present within it. The malleability of its structure, while desirable for display purposes, poses a problem when it comes to data storage. To address this issue, a cross-tab can be represented in a relational form with a fixed number of columns or by introducing a special value, "all," to denote subtotals.

![49](https://user-images.githubusercontent.com/124214430/228470969-7a175849-a9b8-47ae-9057-432361841a7e.png)

![50](https://user-images.githubusercontent.com/124214430/228471006-c8ff957d-2a1d-4511-b778-be265721e33c.png)

Furthermore, hierarchies can be represented in a relational format as well, such as the relationship between womenswear and menswear categories and their respective items. OLAP systems were first implemented using multidimensional arrays in memory, which led to the advent of multidimensional OLAP (MOLAP) systems. Subsequently, OLAP facilities were integrated into relational systems to form relational OLAP (ROLAP) systems. Hybrid systems, also known as hybrid OLAP (HOLAP) systems, arose from storing some summaries in memory and the remaining data in a relational database.

```
select * 
from sales 
pivot ( 
sum(quantity) 
for color in (’dark’,’pastel’,’white’)
) 
order by item name;
```

To compute data cubes, a na¨ıve algorithm requires multiple scans of the relation, which can be optimized by computing an aggregation on a set of attributes from another aggregate with a larger set of attributes. The number of groupings on subsets of dimension attributes in data cubes grows exponentially, making pre-computation and storage of all possible groupings infeasible. Instead, a selected set of groupings can be precomputed and stored, while others can be computed on demand.

![51](https://user-images.githubusercontent.com/124214430/228471041-8622d0bd-0213-4439-818e-7f231f0bcec3.png)

![52](https://user-images.githubusercontent.com/124214430/228471058-c20995ac-178b-4aae-a3b9-98df19196f82.png)

In sum, the nuances of cross-tab and relational tables, as well as OLAP systems, have been the focus of many studies in the realm of database management. Despite the challenges posed by the malleability of cross-tab structures and the exponential growth of groupings in data cubes, researchers have developed optimized methods to address these issues and enhance the efficiency of OLAP systems.

In the ever-evolving world of data management, Online Analytical Processing (OLAP) continues to garner widespread attention. One notable implementation of OLAP is SQL, which boasts a pivot clause that enables the creation of cross-tabs. Supported by a variety of SQL implementations, such as Microsoft SQL Server and Oracle the pivot clause is especially handy for generating a pivot table.

The pivot clause enables the specification of values from an attribute, which are then displayed as attribute names in the pivoted result. It is noteworthy that while the pivot clause does not compute subtotals on its own, it can be used in combination with the group by construct to achieve the desired result.

SQL also supports generalizations of the group by constructing through the cube and rollup operations. The cube and rollup constructs allow for the execution of multiple groups by queries in a single query, with the result returned as a single relation.

Data cube relations can be incredibly large, as evidenced by the cube query, which generates 80 tuples for just 3 possible colors, 4 possible item names, and 3 sizes. To produce a more readable result, the relation of Figure uses "all" in place of null. To achieve the same result, the "all" value must be substituted for null in the query.

![53](https://user-images.githubusercontent.com/124214430/228471094-4ea34639-7c54-40c8-b272-08d4e4cc9ceb.png)

The concept of using the decode function in SQL queries has been explored in depth, with its ability to substitute values in an attribute of a tuple being particularly noteworthy. By comparing a given value against a set of match values and corresponding replacement values, the decode function can effectively replace attribute values as needed. However, it does not function optimally when dealing with null values, as predicates on nulls ultimately result in false. To circumvent this issue, the grouping function can be employed, returning 1 if its argument is a null value generated by a cube or rollup, and 0 otherwise. This allows for the substitution of all values in place of nulls.

```
select decode(grouping(item name), 1, ’all’, item name) as item name 
                decode(grouping(color), 1, ’all’, color) as color 
                sum(quantity) as quantity 
                from sales 
                group by cube(item name, color);
```

In addition to the decode function, the rollup construct has also been discussed. Similar to the cube construct, rollup generates fewer groups by queries and can be useful for hierarchies when groups are of frequent practical interest. 

```
select item name, color, clothes size, sum(quantity) 
        from sales 
        group by rollup(item name), rollup(color, clothes size);
```

For example, a location hierarchy could be grouped by region, country, state, and city, allowing for a sequence of "drilling down" for further detail. Multiple rollups and cubes can also be used in a single group by clause, with the resulting groupings depending on the attributes used in each rollup or cube. While neither clause allows for complete control over the generated groupings, more restricted groupings can be generated using the grouping construct in the having clause.

## Formal Relational Query Languages
In this latest chapter, we examine the very foundations upon which these powerful tools are built. In this illuminating chapter, we explore three formal languages that provide the theoretical framework for SQL and other relational query languages. The first is relational algebra, a powerful tool that underpins the SQL query language and enables it to manipulate and process vast amounts of data with ease. Following this, we delve into the tuple relational calculus and the domain relational calculus, two declarative query languages that are rooted in the realm of mathematical logic. Together, these three formal languages offer a deep understanding of the principles behind modern relational databases, making this chapter an essential resource for anyone looking to gain complete mastery of the subject.

### The Relational Algebra 
In this chapter, we delve into relational algebra, which serves as a procedural query language in the relational database model. With a set of operations that take one or two relations as input and produce a new relation as output, relational algebra offers a variety of useful tools for database querying. The fundamental operations in relational algebra include select, project, union, set difference, Cartesian product, and rename. Additionally, there are other operations available such as set intersection, natural join, and assignment.

![54](https://user-images.githubusercontent.com/124214430/228471133-7b30141e-1604-4583-811b-d74e7daa5475.png)

Unary operations such as select, project, and rename operate on one relation, while binary operations such as union, set difference, and Cartesian product operate on pairs of relations. The select operation, denoted by the lowercase Greek letter sigma (S), selects tuples that satisfy a given predicate. In order to select tuples from the instructor relation where the instructor is in the “Physics” department, one would write dept name = “Physics” (instructor).

To find all instructors with a salary greater than $90,000, one would write salary>90000 (instructor). The selection predicate may include comparisons between two attributes, and multiple predicates can be combined with the connectives and (∧), or (∨), and not (¬).

![55](https://user-images.githubusercontent.com/124214430/228471298-53270837-b1d6-4333-aae3-5f81b78b5bb6.png)

It should be noted that the term selects in relational algebra has a different meaning than in SQL, where it corresponds to what is referred to as where in SQL. This difference in interpretation may lead to confusion, and thus, it is important to differentiate between the two.

The project operation serves as a valuable tool to extract desired information from a relation. Specifically, the project operation allows for the creation of a new relation that retains only selected attributes of the original relation, effectively filtering out any unnecessary data. As a unary operation, projection is denoted by the uppercase Greek letter pi (π) and takes as its argument the relation to be projected. It is important to note that since a relation is a set, any duplicate rows will be eliminated from the resulting relation.

In the case of more complex queries, relational-algebra operations can be composed together to form a relational-algebra expression, akin to the composition of arithmetic operations. In this regard, the result of a relational-algebra operation is of the same type as its inputs, a relation, allowing for seamless integration of operations into a cohesive expression. 

Another key operation in relational algebra is the union operation, represented by the symbol ∪. This operation is essential when combining two relations to form a larger relation that contains all the tuples in both relations, ensuring compatibility between the relations. However, it is crucial to ensure that the relations being combined have the same arity and domains to avoid confusion and errors.

![57](https://user-images.githubusercontent.com/124214430/228471342-2aa8a808-ca13-4784-89d5-d26f1c2e8f13.png)

![58](https://user-images.githubusercontent.com/124214430/228471382-b4c2b7e1-ece0-4d6e-ac00-aefa60aef8c6.png)

In essence, the use of relational-algebra operations provides a powerful toolset for managing and analyzing data in a relational database, allowing for efficient data extraction and manipulation.

In the vast landscape of relational databases, two fundamental operations play a crucial role in combining and comparing data from different sources: the set-difference operation and the Cartesian-product operation. These operations, both part of the relational algebra, are essential tools in the arsenal of database professionals, enabling them to extract valuable insights and make informed decisions based on disparate sets of data.

![59](https://user-images.githubusercontent.com/124214430/228471422-bcb70d86-08fa-46c5-9986-2281cb53e846.png)

The set-difference operation, denoted by the symbol "-", allows us to find tuples that exist in one relation but not in another. By applying this operation, we can discover all courses taught during the Fall 2009 semester but not in the Spring 2010 semester. However, it is important to note that for this operation to be valid, the relations involved must have the same arity and identical domains for each attribute. These conditions ensure that the set difference operation produces meaningful and relevant results.

The Cartesian-product operation, denoted by the symbol "×", is another essential operation in the world of relational databases. This operation enables us to combine information from any two relations, making it possible to create powerful new datasets that contain valuable insights. However, because the same attribute name may appear in both relations, it is necessary to devise a naming scheme that distinguishes between these attributes. We can accomplish this by attaching the name of the relation from which the attribute originates. Moreover, it is essential to ensure that the relations used in this operation have distinct names to avoid any ambiguity.

![60](https://user-images.githubusercontent.com/124214430/228471451-5668fb28-982f-453a-95cb-45c118af7fec.png)

The combination of these operations can be used to extract meaningful data from large datasets. For example, by applying the Cartesian-product operation to the instructor and teaches relations, we can find the names of all instructors in the Physics department, along with the course ID of all the courses they taught. While the Cartesian-product operation may produce some redundancy in the resulting dataset, it remains a powerful tool for database professionals seeking to extract useful information from large and complex datasets.

![61](https://user-images.githubusercontent.com/124214430/228471482-9bd6937e-b433-4190-b3b4-146ee9bc5e60.png)

### The Tuple Relational Calculus 
### The Domain Relational Calculus 

# DATABASE DESIGN

## Database Design and the E-R Model

### Overview of the Design Process
### The Entity-Relationship Model
### Constraints
### Removing Redundant Attributes in Entity Sets
### Entity-Relationship Diagrams
### Reduction to Relational Schemas
### Entity-Relationship Design Issues
### Extended E-R Features
### Alternative Notations for Modeling Data
### Other Aspects of Database Design

## Relational Database Design

### Features of Good Relational Designs
### Atomic Domains and First Normal Form
### Decomposition Using Functional Dependencies
### Functional-Dependency Theory
### Algorithms for Decomposition
### Decomposition Using Multivalued Dependencies
### More Normal Forms
### Database-Design Process
### Modeling Temporal Data

## Application Design and Development

### Application Programs and User Interfaces
### Web Fundamentals
### Servlets and JSP
### Application Architectures
### Rapid Application Development
### Application Performance
### Application Security
### Encryption and Its Applications

# DATA STORAGE AND QUERYING

## Storage and File Structure

### Overview of Physical Storage Media
### Magnetic Disk and Flash Storage
### RAID
### Tertiary Storage
### File Organization
### Organization of Records in Files
### Data-Dictionary Storage
### Database Buffer

## Indexing and Hashing

### Basic Concepts
### Ordered Indices
### B+-Tree Index Files
### B+-Tree Extensions
### Multiple-Key Access
### Static Hashing
### Dynamic Hashing
### Comparison of Ordered Indexing and Hashing
### Bitmap Indices
### Index Deﬁnition in SQL

## Query Processing

### Overview
### Measures of Query Cost
### Selection Operation
### Sorting
### Join Operation
### Other Operations
### Evaluation of Expressions

## Query Optimization

### Overview
### Transformation of Relational Expressions
### Estimating Statistics of Expression Results
### Choice of Evaluation Plans
### Materialized Views**
### Advanced Topics in Query Optimization**

# TRANSACTION MANAGEMENT

## Transactions

### Transaction Concept
### Simple Transaction Model
### Storage Structure
### Transaction Atomicity and Durability
### Transaction Isolation
### Serializability
### Transaction Isolation and Atomicity
### Transaction Isolation Levels
### Implementation of Isolation Levels
### Transactions as SQL Statements

## Concurrency Control

### Lock-Based Protocols
### Deadlock Handling
### Multiple Granularity
### Timestamp-Based Protocols
### Validation-Based Protocols
### Multiversion Schemes
### Snapshot Isolation
### Insert Operations, Delete Operations, and Predicate Reads
### Weak Levels of Consistency in Practice
### 0Concurrency in Index Structures**

## Recovery System

### Failure Classiﬁcation
### Storage
### Recovery and Atomicity
### Recovery Algorithm
### Buffer Management
### Failure with Loss of Nonvolatile Storage
### Early Lock Release and Logical Undo Operations
### ARIES**
### Remote Backup Systems

# SYSTEM ARCHITECTURE

## Database-System Architectures

### Centralized and Client–Server Architectures
### Server System Architectures
### Parallel Systems
### Distributed Systems
### Network Types

## Parallel Databases

### Introduction
### I/O Parallelism 
### Interquery Parallelism
### Intraquery Parallelism
### Intraoperation Parallelism
### Interoperation Parallelism
### Query Optimization
### Design of Parallel Systems
### Parallelism on Multicore Processors

## Distributed Databases

### Homogeneous and Heterogeneous Databases
### Distributed Data Storage
### Distributed Transactions
### Commit Protocols
### Concurrency Control in Distributed Databases
### Availability
### Distributed Query Processing
### Heterogeneous Distributed Databases
### Cloud-Based Databases
### Directory Systems

# DATA WAREHOUSING, DATA MINING, AND INFORMATION RETRIEVAL

## Data Warehousing and Mining

### Decision-Support Systems
### Data Warehousing
### Data Mining
### Classiﬁcation
### Association Rules
### Other Types of Associations
### Clustering
### Other Forms of Data Mining

## Information Retrieval

### Overview
### Relevance Ranking Using Terms
### Relevance Using Hyperlinks
### Synonyms, Homonyms, and Ontologies
### Indexing of Documents
### Measuring Retrieval Effectiveness

# SPECIALTY DATABASES

## Object-Based Databases

### Overview
### Complex Data Types
### Structured Types and Inheritance in SQL
### Table Inheritance
### Array and Multiset Types in SQL
### Object-Identity and Reference Types in SQL
### Implementing O-R Features
### Persistent Programming Languages
### Object-Relational Mapping
### Object-Oriented versus Object-Relational

## XML

### Motivation 
### Structure of XML Data 
### XML Document Schema 
### Querying and Transformation 
### Application Program Interfaces to XML 
### Storage of XML Data 
### XML Applications

# ADVANCED TOPICS

## Advanced Application Development

### Performance Tuning
### Performance Benchmarks
### Other Issues in Application Development
### Standardization

## Spatial and Temporal Data and Mobility

### Motivation
### Time in Databases 
### Spatial and Geographic Data 
### Multimedia Databases 
### Mobility and Personal Databases

## Advanced Transaction Processing

### Transaction-Processing Monitors
### Transactional Workﬂows 
### E-Commerce
### Main-Memory Databases
### Real-Time Transaction Systems
### Long-Duration Transactions

# CASE STUDIES

## PostgreSQL

### Introduction
### User Interfaces
### SQL Variations and Extensions
### Transaction Management in PostgreSQL
### Storage and Indexing
### Query Processing and Optimization
### System Architecture

## Oracle

### Database Design and Querying Tools
### SQL Variations and Extensions
### Storage and Indexing
### Query Processing and Optimization
### Concurrency Control and Recovery
### System Architecture
### Replication, Distribution, and External Data
### Database Administration Tools
### Data Mining

## IBM DB2 Universal Database

### Overview
### Database-Design Tools
### SQL Variations and Extensions
### Storage and Indexing
### Multidimensional Clustering
### Query Processing and Optimization
### Materialized Query Tables
### Autonomic Features in DB2
### Tools and Utilities
### Concurrency Control and Recovery
### System Architecture
### Replication, Distribution, and External Data
### Business Intelligence Features 1221 Bibliographical Notes

## Microsoft SQL Server

### Management, Design, and Querying Tools
### SQL Variations and Extensions
### Storage and Indexing
### Query Processing and Optimization
### Concurrency and Recovery
### System Architecture
### Data Access
### Distributed Heterogeneous Query Processing
### Replication
### Server Programming in .NET
### XML Support
### SQL Server Service Broker
### Business Intelligence
