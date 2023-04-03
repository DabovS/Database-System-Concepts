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

```Type instructor = record
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

```         select instructor.name
            from instructor 
            where instructor.dept name = ’History’;
```

The expected result of running a specific SQL query on the tables in Figure 1.2. The query is designed to find the names of all instructors in the History department. The system would search the tables and find that there are two departments with a budget greater than $95,000: Computer Science and Finance. There are a total of five instructors in these departments, so the resulting table would have two columns (ID, dept name) and five rows listing the instructors in the two departments.

```Create table department
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

```department (dept name, building, budget)

```

The schema of a relation generally does not change, whereas the contents of a relation instance may change as the relation is updated.

```section (course id, sec id, semester, year, building, room number, time slot id)
```

Common attributes in relation schemas are used to relate tuples of distinct relations.

```teaches (ID, course id, sec id, semester, year)
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

```create table department
(dept name varchar (20), 
building varchar (15), 
budget numeric (12,2),
primary key (dept name));
```

An example of creating a relation in SQL with three attributes - dept name, building, and budget. The data types for these attributes are specified as character string of maximum length 20, character string of maximum length 15, and number with 12 digits in total, 2 of which are after the decimal point, respectively. The primary key for this relation is set to be the dept name attribute.

```create table r
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

```drop table r;
```

```delete from r;
```

* SQL commands for modifying the structure of a relation, including deleting tuples or dropping a relation entirely using the DELETE and DROP TABLE commands, respectively.
* The ALTER TABLE command for adding attributes to an existing relation, with all tuples assigned null as the value for the new attribute.

```alter table r add AD;
```

The alter table command allows us to add a new attribute to an existing relation named r, where A is the name of the attribute to be added and D is the type of the new attribute. In contrast, we can remove attributes from a relation using the drop command.

```alter table r drop A;
```

In SQL, an attribute can be dropped from an existing relation by using the *alter table* command. However, many database systems do not support this functionality, and instead only allow an entire table to be dropped.

### Basic Structure of SQL Queries

The basic structure of an SQL query consists of three clauses: select, from, and where. The query operates on the relations listed in the from clause, performs operations on them as specified in the where and select clauses, and produces a relation as the result.

![22](https://user-images.githubusercontent.com/124214430/228469256-9c55d23e-d479-4fa6-9d8a-b126c14f47ba.png)

In the case of a query on a single relation, the example given is to find the names of all instructors in the university example. The instructor relation is listed in the from clause and the name attribute is specified in the select clause.

```select name
from instructor;
```

The basic structure of an SQL query consists of three clauses: select, from, and where. The select clause specifies the attributes of the relation to be displayed in the output, the from clause specifies the input relation, and the where clause is used for filtering the tuples.

```select dept name
from instructor;
```

SQL allows duplicate tuples in relations and in the results of SQL expressions. In order to force the elimination of duplicates, the keyword "distinct" is inserted after select.

```select distinct dept name
from instructor;
```

![23](https://user-images.githubusercontent.com/124214430/228469303-8d089028-869e-4cd3-bbf6-c15f57cb07ad.png)

The SQL keyword "distinct" can be used to eliminate duplicates in query results, while "all" can be used to specify that duplicates should be retained. The select clause in SQL queries can include arithmetic expressions that involve mathematical operators and constants or attributes of tuples.

```select all dept name
from instructor;
```

The where clause allows the selection of specific rows in the query result based on a specified predicate.

```select ID, name, dept name, salary *1.1
from instructor;
```

The SQL language allows us to manipulate data in a relational database. We can use arithmetic expressions to modify the values of attributes or create new attributes, but this does not modify the original relation.

![24](https://user-images.githubusercontent.com/124214430/228469344-a8975781-6fae-4f34-84b7-50f40ca5d6c8.png)

```select name
from instructor 
where dept name = ’Comp. Sci.’ and salary > 70000;
```

SQL also provides special data types and arithmetic functions to operate on them. We can use the WHERE clause to filter the results of a query and retrieve only those tuples that satisfy a specified predicate. 

![25](https://user-images.githubusercontent.com/124214430/228469380-10560e40-0ac5-4ea1-a500-816d2ceac65a.png)

Logical connectives such as AND, OR, and NOT can be used in the WHERE clause along with comparison operators to compare strings and arithmetic expressions. In queries involving multiple relations, we need to specify the relations to be accessed in the FROM clause and specify the matching condition in the WHERE clause. The SELECT clause is used to retrieve the desired attributes from the selected tuples.

This section discusses SQL queries that involve multiple relations. It explains that in such cases, the naming convention requires that relations in the from clause have distinct names. The select clause is used to list the desired attributes in the query result, the from clause is a list of the relations to be accessed, and the where clause is a predicate involving attributes of the relations in the from clause. The general form of an SQL query is given, which includes attributes, relations, and a predicate. If the where clause is omitted, the predicate is true.

```select A1, A2,..., An
from r1, r2,...,rm 
where P;
```

The order of the clauses in an SQL query must be select, from, and then where, but it can be easier to understand the operations if they are considered in the order from, where, and then select. The from clause generates tuples for the result relation of the from clause by defining a Cartesian product of the relations listed in the clause.

```for each tuple t1 in relation r1
    for each tuple t2 in relation r2
        ... 
            for each tuple tm in relation rm
                Concatenate t1, t2,..., tm into a single tuple t
                Add t into the result relation
```

This is done iteratively, creating a new tuple by concatenating each tuple in each relation, and then adding that tuple to the result relation. The result relation has all attributes from all the relations in the from clause, and since the same attribute name may appear in multiple relations, the name of the relation from which the attribute originally came must be prefixed before the attribute name.

The naming convention used in SQL queries involving multiple relations:

```(instructor.ID, instructor.name, instructor.dept name, instructor.salary teaches.ID, teaches.course id, teaches.sec id, teaches.semester, teaches.year)
```

Attributes that appear in only one relation do not need to be pre-fixed with the relation name. However, when the same attribute name appears in multiple relations, the naming convention requires that the attribute be prefixed with the relation name to avoid ambiguity.

```(instructor.ID, name, dept name, salary teaches.ID, course id, sec id, semester, year)
```

The Cartesian product of relations is defined as a set of tuples generated by iterating through each tuple in each relation listed in the from clause. The resulting relation has all the attributes from all the relations in the from clause. The article illustrates the Cartesian product of the instructor and teaches relations and explains that combining tuples from unrelated relations can result in an extremely large relation, making it rarely sensible to create such a Cartesian product.

![26](https://user-images.githubusercontent.com/124214430/228469433-26cd5483-2267-4a9f-ae47-3a13f146ef6b.png)

To use the WHERE clause in an SQL query to restrict the output to meaningful results. The WHERE clause is used to combine tuples from different tables based on common attributes.

```select name, course id
from instructor, teaches 
where instructor.ID= teaches.ID;
```

SQL query combines tuples from the instructor and teaches tables to output instructor names and course IDs. The output only includes instructors who have taught some course, and instructors who have not taught any course are excluded.

```select name, course id
from instructor, teaches 
where instructor.ID= teaches.ID and instructor.dept name = ’Comp. Sci.’;
```

To add an extra predicate to the WHERE clause to further restrict the output:

![27](https://user-images.githubusercontent.com/124214430/228469489-31b44bc7-df6e-4307-9ae1-d37e16904a26.png)

The sequence of steps involved in executing an SQL query, which involves generating a Cartesian product of the relations listed in the FROM clause, applying predicates specified in the WHERE clause, and outputting the selected attributes. However, a real implementation of SQL optimizes the evaluation process to generate only the elements of the Cartesian product that satisfy the WHERE clause predicates. Also the consequences of omitting appropriate WHERE clause conditions can lead to the output of a huge relation.

The natural join operation in SQL produces a relation as a result by considering only those pairs of tuples with the same value on the common attributes that appear in the schemas of both relations. SQL also supports other ways of joining information from multiple relations.

![28](https://user-images.githubusercontent.com/124214430/228469544-ebdabc23-180d-48c3-8c64-883429eb894a.png)

The natural join operation in SQL combines information from two relations based on the matching of attributes with the same name.

```select name, course id
from instructor, teaches 
where instructor.ID= teaches.ID;
```

It produces a relation that contains only those tuples with the same value on the common attribute.

```select name, course id
from instructor natural join teaches;
```

The resulting relation has only those attributes that are common to the schemas of both relations, followed by those that are unique to the schema of each relation.

```select A1, A2,..., An
from r1 natural join r2 natural join ... natural join rm 
where P;
```

The natural join can be used in SQL queries with the from clause to combine multiple relations.

```from E1, E2,..., En
```

The select and where clauses are then evaluated on the resulting relation.

```select name, title
from instructor natural join teaches, course 
where teaches.course id= course.course id;
```

The natural join is a useful tool for simplifying SQL queries and reducing the size of the output.

SQL operations, specifically natural join and rename operations.

```select name, title
from instructor natural join teaches natural join course;
```

```select name, title
from (instructor natural join teaches) join course using (course id);
```

### Additional Basic Operations

```select name, course id
from instructor, teaches 
where instructor.ID= teaches.ID
```

```name, course id
```

The natural join operation combines two tables by matching attributes with the same name, while the rename operation allows renaming of table attributes using the "as" clause.

```name, course id
```

```old-name as new-name
```

Natural join while avoiding equating attributes erroneously and how the rename operation is useful in renaming relations.

```select name as instructor name, course id from instructor, teaches
where instructor.ID= teaches.ID;
```

```select T.name, S.course id
from instructor as T, teaches as S 
where T.ID= S.ID;
```

SQL queries use these operations to obtain specific results.

SQL queries and a few examples below of different operations that can be performed on character strings:

```select distinct T.name
from instructor as T, instructor as S 
where T.salary > S.salary and S.dept name = ’Biology’;
```

Also, the use of correlation names or table aliases in SQL. SQL strings are enclosed in single quotes and that the equality operation on strings is case sensitive.

```select dept name
from department 
where building like ’%Watson%’;
```

SQL also permits a variety of functions on character strings, such as concatenation, substring extraction, and string length calculation. To perform pattern matching using the like operator and how to specify an escape character for special pattern characters.

```like ’ab\%cd%’ escape ’\’ matches all strings beginning with “ab%cd”
like ’ab\\cd%’ escape ’\’ matches all strings beginning with “ab\cd”

```

Finally, some databases provide variants of the like operation which do not distinguish between lower and upper case, and SQL:1999 offers a similar to operation that provides more powerful pattern matching.

In SQL, the asterisk symbol (*) is used in the select clause to indicate "all attributes" of a table.

```select instructor.*
from instructor, teaches 
where instructor.ID= teaches.ID;
```

The order by clause can be used to sort the tuples in the result of a query in ascending or descending order, and can be performed on multiple attributes.

```select name
from instructor 
where dept name = ’Physics’ order by name;
```

The between comparison operator simplifies where clauses that specify a value range, and the not between operator can also be used.

```select *
from instructor 
order by salary desc, name asc;
```

To find instructor names and the courses they taught for instructors in the Biology department who have taught some course, an extra condition can be added to the where clause.

```select name
from instructor 
where salary between 90000 and 100000;
```

instead of:

```select name
from instructor 
where salary <= 100000 and salary >= 90000;
```

Below are various SQL operations such as attribute specification, ordering of tuples, where clause predicates, and set operations:

```select name, course id
from instructor, teaches 
where instructor.ID= teaches.ID and dept name = ’Biology’;
```

```select name, course id
from instructor, teaches 
where (instructor.ID, dept name) = (teaches.ID, ’Biology’);
```

```select name, course id
from instructor, teaches 
where (instructor.ID, dept name) = (teaches.ID, ’Biology’);
```

![29](https://user-images.githubusercontent.com/124214430/228469679-bf0f8fa7-0991-4291-b05f-0bb1cc937e65.png)

The asterisk symbol (*) is used in the select clause to indicate "all attributes."

```select name, course id
from instructor, teaches 
where (instructor.ID, dept name) = (teaches.ID, ’Biology’);
```

### Set Operations

Ordering of tuples can be performed using the order by clause, and we can specify the sort order using desc for descending order or asc for ascending order.

```select course id
from section 
where semester = ’Fall’ and year= 2009;
```

```select course id
from section 
where semester = ’Spring’ and year= 2010;

```

![30](https://user-images.githubusercontent.com/124214430/228469710-78a79466-4af6-4aaf-8040-87dde5c5df00.png)

The between comparison operator can be used to simplify where clauses that specify a value between two values. The SQL operations union, intersect, and except are used for set operations.

```(select course id
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

```(select course id
from section 
where semester = ’Fall’ and year= 2009) 
union all
(select course id 
from section 
where semester = ’Spring’ and year= 2010);
```

```(select course id
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

```(select course id
from section 
where semester = ’Fall’ and year= 2009) 
intersect all
(select course id 
from section 
where semester = ’Spring’ and year= 2010);
```

The intersect operation finds the common elements between two sets, and it automatically eliminates duplicates. But, if we want to keep duplicates, we must use intersect all instead of intersect. Finally, the except operation finds the difference between two sets, and it automatically eliminates duplicates.

```(select course id
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

```(select course id
from section 
where semester = ’Fall’ and year= 2009)
union all
(select course id
from section
where semester = ’Spring’ and year= 2010);
```

```(select course id
from section 
where semester = ’Fall’ and year= 2009) 
intersect
(select course id 
from section 
where semester = ’Spring’ and year= 2010);
```

The union operation combines the results of two queries, and it eliminates duplicates by default. However, if we want to retain duplicates, we must use union all instead of union.

![33](https://user-images.githubusercontent.com/124214430/228469871-767b258f-a4d9-4e92-878e-b79251d96e7f.png)

```(SELECT course.id
FROM section
WHERE semester = 'Fall' AND year = 2009)
INTERSECT ALL
(SELECT course.id
FROM section
WHERE semester = 'Spring' AND year = 2010);
```

The intersect operation finds the common elements between two sets, and it automatically eliminates duplicates. But, if we want to keep duplicates, we must use intersect all instead of intersect. Finally, the except operation finds the difference between two sets, and it automatically eliminates duplicates. 

```(select course id
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

```select name
from instructor 
where salary is null;
```

When using the select distinct clause, identical tuples must be removed. To accomplish this, SQL treats values of corresponding attributes from two tuples as the same if they are both non-null and equal in value or both null. Therefore, two copies of a tuple such as {(’A’, null), (’A’, null)} are considered identical, even if some of the attributes have null values. By using the distinct clause, only one copy of these identical tuples can be retained. It is important to note that nulls are treated differently in predicates, where a comparison “null=null” yields unknown instead of true. This approach of treating tuples as identical is also employed in the set operations union, intersection, and except.

In short, dealing with null values in relational operations requires careful handling and an understanding of how SQL operates with unknown values.

### Aggregate Functions

SQL provides a powerful set of tools for querying and manipulating data stored in relational databases. One of the most important features of SQL is its support for aggregate functions, which allow users to perform computations on collections of values and return a single result. The five built-in aggregate functions in SQL are average, minimum, maximum, total, and count, each of which takes a set or multiset of values as input and returns a single value.

```select avg (salary)
from instructor 
where dept name= ’Comp. Sci.’;
```

Basic aggregation in SQL involves computing an aggregate function on a set of tuples and returning a single tuple as the result. For example, we can use the AVG function to compute the average salary of instructors in the Computer Science department by writing a SQL query that selects the average salary from the instructor table and restricts the results to instructors in the Computer Science department.

```select avg (salary) as avg salary
from instructor 
where dept name= ’Comp. Sci.’;
```

![34](https://user-images.githubusercontent.com/124214430/228469997-5f1e7b1b-9a2d-46b8-adb8-230dc4a74410.png)

In more complex cases, we may need to group the tuples in the input relation into subsets based on the values of one or more attributes, and then compute an aggregate function on each subset. This is accomplished using the GROUP BY clause in SQL. For example, we can use the GROUP BY clause to compute the average salary of instructors in each department by grouping the tuples in the instructor table by department name and then computing the average salary for each group.

```select count (distinct ID)
from teaches 
where semester = ’Spring’ and year = 2010;
```

```select count (*)
from course;
```

![35](https://user-images.githubusercontent.com/124214430/228470024-20cf3891-ed34-4ccd-ab8b-000cd97da0c3.png)

When using the GROUP BY clause, it is important to ensure that any attribute that appears in the SELECT clause but is not part of the GROUP BY clause is enclosed in an aggregate function, to avoid ambiguity in the query. Similarly, we can use the DISTINCT keyword in the COUNT function to eliminate duplicate values before performing the computation. These powerful features of SQL make it a valuable tool for managing and analyzing large datasets in a variety of contexts.

```select dept name, avg (salary) as avg salary
from instructor 
group by dept name;
```

```select avg (salary)
from instructor;
```

![36](https://user-images.githubusercontent.com/124214430/228470070-310dd7b6-8ec4-44c0-ae68-f9c50a1a2463.png)

### Nested Subqueries

Structured Query Language (SQL) provides a powerful mechanism for nesting subqueries, a technique that allows select-from-where expressions to be embedded within other queries. This capability is frequently employed to perform a range of operations, including set membership tests, set comparisons, and set cardinality evaluations.

One common use of nested subqueries is to test for set membership using the in-connective, which tests whether a given tuple belongs to a relation. This is achieved by constructing a set of values using a select clause and testing for membership using the in operator. Conversely, the not-in operator is used to test for the absence of set membership.

```select distinct course id
from section 
where semester = ’Fall’ and year= 2009 and
        course id in (select course id 
            from section 
            where semester = ’Spring’ and year= 2010);
```

SQL’s flexibility enables users to craft queries using different approaches to arrive at the same results. For example, consider the query "Find all the courses taught in both the Fall 2009 and Spring 2010 semesters." The not-in construct is similarly used to test for membership in the absence of a set. The ability to test for membership in arbitrary relations further extends the capabilities of SQL.

```select distinct course id
from section 
where semester = ’Fall’ and year= 2009 and
course id not in (select course id 
        from section 
        where semester = ’Spring’ and year= 2010);
```

In summary, the power and flexibility of SQL's nested subqueries enable sophisticated set manipulations and set comparisons, making it a highly valuable tool for data management and analysis.

In the vast realm of data manipulation, SQL provides a powerful tool for the discerning data analyst - the nested subquery. Such a subquery is essentially a select-from-where expression that is nested within another query, and it can be used to perform tests for set membership, make set comparisons and determine set cardinality.

One particularly interesting use of nested subqueries is to test for set membership using the 'in' connective in the where clause. For example, to find all courses taught in both the Fall 2009 and Spring 2010 semesters, we can first find all courses taught in the latter semester using a subquery, and then nest that subquery in the where clause of an outer query to find those courses that were also taught in Fall 2009. The resulting query is both flexible and efficient, allowing the user to approach the problem in a way that seems most natural.

```select distinct course id
from section 
where semester = ’Fall’ and year= 2009 and
course id not in (select course id 
        from section 
        where semester = ’Spring’ and year= 2010);
```

Nested subqueries can also be used to compare sets, as in the query "Find the names of all instructors whose salary is greater than at least one instructor in the Biology department." This can be written using the > some construct, which generates the set of all salary values of instructors in the Biology department and compares them to the salary values of the instructors in the outer query.

```select distinct T.name
from instructor as T, instructor as S 
where T.salary > S.salary and S.dept name = ’Biology’;
```

```select name
from instructor 
where salary > all (select salary 
                    from instructor 
                    where dept name = ’Biology’);
```

SQL offers a wide range of options for testing set membership and comparison using nested subqueries, making it an indispensable tool for data analysts in their quest for insights and knowledge.

In the world of database management, SQL is the lingua franca, enabling users to execute complex queries and sift through mountains of data with ease. But beyond its standard comparison operators, SQL boasts a number of lesser-known, yet equally powerful features that can be harnessed to produce sophisticated results.

```select dept name
from instructor 
group by dept name 
having avg (salary) >= all (select avg (salary)
                            from instructor 
                            group by dept name)
```

For instance, by using set comparisons, one can identify departments with the highest average salary, or courses taught in both the Fall 2009 and Spring 2010 semesters. These queries involve the use of subqueries, including correlated subqueries, and scoping rules to ensure that the right data is being accessed.

Additionally, SQL includes features for testing empty relations, checking for duplicate tuples, and testing the absence of duplicate tuples. With the "exists" construct, one can test whether a subquery has any tuples in its result, while the "unique" construct returns true if the argument subquery contains no duplicate tuples.

```select T.course id
from course as T 
where unique (select R.course id 
                from section as R 
                where T.course id= R.course id and
                R.year = 2009);
```

By utilizing these advanced features of SQL, users can gain greater insights into their data and extract more value from it. It is a testament to the power and versatility of this programming language that it remains a vital tool in the ever-expanding world of big data.

### Modification of the Database

In the world of database management, the ability to add, remove, or change information is a critical aspect of data processing. While we have thus far focused on information extraction, the manipulation of data is an equally vital function, made possible through the power of SQL.

Deletion is a key operation that can be expressed in a way that is similar to a query, allowing for the removal of entire tuples. It is important to note that only whole tuples can be deleted; values on specific attributes cannot be removed.

```delete from r
where P;
```

The predicate in the "where" clause can be as complex as that of a select command’s "where" clause. The request "delete from instructor" is an example of deleting all tuples from the "instructor" relation. However, the "instructor" relation itself still exists but is emptied of all tuples.

```delete from instructor
where dept name in (select dept name 
from department 
where building = ’Watson’);
```

Insertion of data is achieved by either specifying a tuple to be inserted or writing a query that results in a set of tuples to be inserted. In both cases, the attribute values for inserted tuples must be members of the corresponding attribute’s domain, and the tuples inserted must have the correct number of attributes.

```insert into student
values (’3003’, ’Green’, ’Finance’, null);
The tuple inserted by this request speciﬁed that a student with ID “3003” is in the Finance department, but the tot cred value for this student is not known. Consider the query:
```

The simplest insert statement involves inserting one tuple, with attribute values specified in the order in which the corresponding attributes are listed in the relation schema.  In more complex cases, we may want to insert tuples on the basis of the result of a query. SQL allows this through the use of the "insert into" statement, followed by a "select" statement that specifies the set of tuples to be inserted. This is particularly useful when inserting data into a relation with a large number of attributes. It is essential to evaluate the "select" statement fully before any insertions are carried out to avoid unexpected results.

```select student
from student where tot cred > 45;
```

Deletion and insertion of data are the two most common operations used for modifying a database, and SQL provides a powerful and flexible way to accomplish these tasks. By using SQL, we can add, remove, or change data with ease, allowing us to better manage and analyze vast amounts of information.

```update instructor
set salary = salary *1.05 where salary < 70000;
```

SQL, the language of relational databases, offers a versatile set of tools for manipulating data in tables. One of the most frequently used operations is the update statement, which modifies the values of selected tuples in a given relation. To identify which tuples to update, SQL uses a where clause that can include any construct legal in the where clause of a select statement, including nested selects.

In the case of a nested select within an update statement, the relation being updated may be referenced. SQL tests all tuples in the relation to see whether they should be updated and carries out the updates afterward.

As a practical example, consider the request “Give a 5 percent salary raise to instructors whose salary is less than average”. This can be expressed in SQL as an update statement that includes a nested select to calculate the average salary of instructors.

```update instructor
set salary = salary *1.05 
where salary < (select avg (salary)
from instructor);

```

```update instructor
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

```Copy code
select * 
from student join takes on student.ID= takes.ID;
```

![39](https://user-images.githubusercontent.com/124214430/228470229-579fa092-2460-45f3-a309-f130532bc2fa.png)

The on condition stipulates that a tuple from the student relation matches a tuple from the takes relation if their ID values are equal. The resulting join expression is similar to the student natural join takes operation, except that the ID attribute is listed twice in the join result, once for the student and once for takes. However, the two ID attributes must have the same value.

Interestingly, the preceding query is equivalent to the following one:

```select *
from student, takes 
where student.ID= takes.ID;
```

As seen earlier, the relation name is used to disambiguate the attribute name ID, allowing us to refer to the two occurrences as students.ID and takes.ID, respectively. A version of the query that displays the ID value only once is:

```select student.ID as ID, name, dept name, tot cred, course id, sec id, semester, year, grade
from student join takes on the student.ID= takes.ID;
```

![40](https://user-images.githubusercontent.com/124214430/228470263-61b913ea-8644-4acc-a85a-9330a3894f56.png)

The query result is depicted in the Figure.

While the on condition allows for more expressive join predicates than the natural join, it may seem redundant since an equivalent expression without the on condition can be written, with the predicate in the on clause moved to the where clause.

### Views

In today's world of data management, it is of utmost importance to ensure that sensitive information is kept secure and out of the reach of unauthorized personnel. In the realm of databases, this can be achieved through the use of views.

Views are virtual relations that can be defined in SQL through the CREATE VIEW command. They allow users to have a customized, personalized collection of relations that is better matched to their needs and intuition than the logical model. For instance, consider a clerk who needs to know an instructor's ID, name, and department, but should not have authorization to view the salary amount. A view relation, such as 'faculty', can be created for the clerk, containing only the necessary attributes.

```select course.course id, sec id, building, room number from course, section
where course.course id = section.course id 
and course.dept name = ’Physics’ 
and section.semester = ’Fall’ 
and section.year = ’2009’;
```

Views are not precomputed and stored, but are computed by executing the query whenever the view is used. Thus, the view relation is created whenever needed, on demand. This ensures that the information is always up to date and accurate, as the tuples are generated by computing the query result each time.

```create view faculty as
select ID, name, dept name 
from instructor;
```

Furthermore, it is possible to create multiple views on top of any given set of actual relations, allowing for a large number of views to be supported. Using the view name, users can refer to the virtual relation that the view generates and use it in SQL queries.

```create view departments total salary(dept name, total salary) as select dept name, sum (salary)
from instructor 
group by dept name;
```

Views in SQL provide a secure and flexible way of accessing and manipulating data, allowing users to have a customized and intuitive collection of relations that are always up to date and accurate.

In the realm of database systems, a compelling technique for querying large volumes of data is through the use of views. These are essentially virtual tables, whose contents are derived from the values of the underlying base relations, but presented to the user in a more intuitive and meaningful manner However, when it comes to modifying the database, the use of views presents serious challenges.

To address the aforementioned challenge, some database systems offer the concept of materialized views. These views not only store the results of the query, but also keep them up-to-date with any changes to the underlying base relations. However, the maintenance of materialized views comes with its own set of concerns, including storage costs and added overhead for updates. Despite these trade-offs, applications that frequently use views, or demand fast response times for large aggregates can benefit greatly from the use of materialized views.

```create view instructor info as
select ID, name, building 
from instructor, department 
where instructor.dept name= department.dept name;
```

![41](https://user-images.githubusercontent.com/124214430/228470304-7a05bc4c-a9ae-41e2-b61d-1bbc53df32e3.png)

On the other hand, modifying the database through views is fraught with difficulties. This is because any change to the database expressed in terms of a view must be translated to a modification to the actual relations in the logical model of the database. For instance, the addition of a tuple through a view raises the question of how to assign a value for the salary attribute, given that it is not present in the view. Similarly, the insertion of a tuple through a view with multiple relations may require the use of nulls, which can lead to unexpected and undesired results.

```insert into instructor info
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

```name varchar(20) not null
budget numeric(12,2) not null
```

There are several types of integrity constraints that can be included in the create table command, such as not null, unique, and check. The not null constraint, for instance, restricts the domain of certain attributes to exclude null values. This constraint prohibits the insertion of a null value for the attribute and generates an error diagnostic if attempted. Similarly, the unique constraint specifies that no two tuples in the relation can be equal on all the listed attributes, with candidate key attributes allowed to be null unless explicitly declared not null.

```unique (Aj1, Aj2,..., Ajm)
```

Overall, the use of integrity constraints is crucial in maintaining data consistency in a database system, and their inclusion in the design process can help prevent costly errors and ensure the reliability of the system.

The SQL language provides a variety of mechanisms to ensure data integrity in relational databases, including the check clause and referential integrity constraints. When used in a relation declaration, the check clause allows the specification of a predicate that must be satisfied by every tuple in the relation, effectively creating a powerful type system that restricts attribute domains in ways that most programming-language type systems cannot. For example, a clause such as "check (budget > 0)" would ensure that the value of the budget attribute in a relation called department is nonnegative.

```create table section
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

```dept name varchar(20) references department
```

While the SQL standard permits the use of subqueries in the predicate of a check clause, none of the widely used database products currently support this feature. Nonetheless, the check clause and referential integrity constraints are valuable tools for ensuring the correctness and consistency of relational data.

In the realm of relational databases, referential-integrity constraints are a critical element in maintaining consistency and accuracy. These constraints act as guardians, ensuring that any updates or modifications to the database do not result in a violation of the data relationships. Typically, when a referential-integrity constraint is violated, the system's standard response is to reject the action, and the transaction performing the update is rolled back. However, with the use of foreign key clauses, a violation of the constraint can be handled differently.

```create table classroom
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

Create table instructor
(ID varchar (5), 
name varchar (20), not null
dept name  varchar (20), 
salary numeric (8,2), check (salary > 29000), 
primary key (ID), 
foreign key (dept name) references department)

Create table section
(course id varchar (8), 
sec id varchar (8), 
semester varchar (6), check (semester in
                                (’Fall’, ’Winter’, ’Spring’, ’Summer’),
year    numeric (4,0), check (year > 1759 and year < 2100))
building varchar (15), 
room number varchar (7), 
time slot id varchar (4), 
primary key (course id, sec id, semester, year), 
foreign key (course id) references course, 
foreign key (building, room number) references classroom)
```

By including a foreign key clause in the schema, developers can specify that instead of rejecting the action, the system must take measures to restore the constraint. For instance, if a tuple is deleted from the referenced relation, causing a violation of the integrity constraint, the system will not reject the deletion. Instead, if a "delete cascade" clause is included in the foreign-key declaration, the system will propagate the deletion to the referencing tuples in the dependent relation. Similarly, an "update cascade" clause will result in the system updating the referencing tuples to reflect the updated value.

It is worth noting that the use of null values in foreign keys can complicate the application of referential-integrity constraints. While null values are allowed for attributes of foreign keys, the system's response to them may not always be the correct choice. Therefore, SQL provides developers with constructs that allow them to specify alternative behaviors when dealing with null values.

```create table course
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

```create assertion credits earned constraint check
(not exists (select ID 
from student 
where tot cred <> (select sum(credits))
from takes natural join course 
where student.ID= takes.ID
and grade is not null and grade<> ’F’ )
```

The world of databases may be complex, but it is an essential aspect of modern-day life. As such, it is important to remain vigilant when maintaining data integrity and to utilize the most effective tools available to do so.

### SQL Data Types and Schemas

We explored integer types, real types, and character types, and now we shall unravel some of the lesser-known data types supported by SQL, in addition to creating basic user-defined types.

Such a set of data types is the date and time types. These allow for the storage of calendar dates and the time of day in hours, minutes, and seconds. A variant of the time type allows for the specification of fractional digits for seconds, and time zone information can also be stored along with the time.

Another data type is the timestamp, which combines date and time. It too has a variant that allows for the specification of the number of fractional digits for seconds, and time-zone information can be included as well.

```date ’2001-04-25’
time ’09:30:00’ 
timestamp ’2001-04-25 10:29:01.45’
```

To specify a date and time value, one can use the format year followed by month followed by day. A string can be converted to the appropriate data type using the cast expression.

```reate table student
(ID varchar (5), 
name varchar (20) not null, 
dept name varchar (20), 
tot cred numeric (3,0) 
default 0, primary key (ID));
```

SQL provides several functions to extract individual fields from a date or time value, and it allows comparison operations on all the types listed here. SQL also offers a data type called interval that enables computations based on dates and times.

Furthermore, SQL permits the specification of default values for attributes, as demonstrated by the create table statement. The default value is set to 0 for the tot cred attribute in this example, and this value is assigned when a tuple is inserted into the student relation without a value for the tot cred attribute.

```insert into student(ID, name, dept name)
values (’12789’, ’Newman’, ’Comp. Sci.’);
```

In essence, SQL's data types and schemas offer a range of options for the storage and manipulation of data, making it a powerful tool in the hands of those who know how to wield it.

In the world of database management, indexing is a crucial tool for efficient querying. With many queries referencing only a small proportion of records, it's wasteful for the system to scan through every tuple of relation to find the desired results. That's where index creation comes in.

```Create index studentID index on student(ID);
```

An index is a data structure that allows a database system to efficiently find tuples in a relation that have a specific value for an attribute, without the need to scan through all the tuples. This is achieved by creating an index on the attribute, allowing the system to retrieve the desired tuples directly.

```book review clob(10KB)
image blob(10MB) 
movie blob(2GB)
```

In addition to single attribute indices, indices can also be created on a list of attributes, such as a combination of name and department name. While the SQL language does not provide syntax for creating indices, many databases offer support for index creation via SQL statements.

When it comes to storing large objects, such as high-resolution medical images or video clips, SQL provides large-object data types. These data types, known as CLOB and BLOB, allow for the storage of kilobyte to gigabyte-scale attributes.

However, retrieving entire large objects into memory can be impractical or inefficient. Instead, applications often use an SQL query to retrieve a locator for a large object and then manipulate the object using the locator. The locator can be used to fetch the large object in small pieces, much like reading data from a file using a read function call.

SQL provides support for user-defined types, enabling the creation of distinct types to enhance data integrity and prevent programming errors. This form of user-defined data types allows for the creation of unique data types that can be used as attributes of relations such as Dollars and Pounds, which are defined as decimal numbers with 12 total digits, two of which are placed after the decimal point.

```create type Dollars as numeric(12,2) ﬁnal;
create type Pounds as numeric(12,2) ﬁnal;
```

By utilizing strong type checking, SQL can identify and prevent programming errors such as assigning a value of type Dollars to a variable of type Pounds, which may be due to a programmer forgetting the differences in currency. Additionally, the use of domains, introduced in SQL-92, can add integrity constraints to an underlying type, such as not null and default values.

```create table department
dept name   varchar (20), 
building varchar (15), 
budget Dollars);
```

Domains differ from user-defined types in that they can have constraints and default values specified on them, while user-defined types are designed to be used in procedural extensions to SQL where it may not be possible to enforce constraints. Furthermore, values of one domain type can be assigned to values of another domain type as long as the underlying types are compatible, whereas user-defined types are strongly typed.

```create domain DDollars as numeric(12,2) not null;
```

```create domain YearlySalary numeric(8,2)
        constraint salary value test check(value >= 29000.00);
```

```create domain degree level varchar(10)
        constraint degree level test 
                check (value in (’Bachelors’, ’Masters’, or ’Doctorate’));
```

SQL's support for user-defined types and domains provides a robust and flexible system for managing complex data structures and enforcing data integrity constraints.

Creating tables with similar schemas as existing tables can prove to be a challenging and time-consuming task for developers. However, SQL offers a useful tool in the form of a "create table-like" extension that can assist in this endeavor. By executing a statement such as "create table temp instructor like the instructor," a new table can be generated with the same schema as an existing one.

```create table temp instructor like instructor;
```

In addition, developers may find it useful to store the result of a complex query as a new table. The SQL:2003 standard provides a simpler and more efficient technique for this task, enabling the creation of a temporary table containing the results of a query with a single statement. This method can be accomplished by executing a command such as "create table t1 as (select * from instructor where dept name= 'Music') with data."

```create table t1 as
    (select * 
        from instructor 
        where dept name= ’Music’)
        with data;
```

It is worth noting that some database management systems may utilize slightly different syntax to execute these tasks. Nevertheless, the create table ... as statement bears resemblance to the create view statement in that both rely on queries for their definitions. The main difference is that the contents of a table are set when the table is created, whereas a view's contents always reflect the current query result.

Early file systems stored all files in a single directory, making it difficult to name files uniquely. Similarly, early database systems had a single namespace for all relations, which led to coordination issues. To solve this problem, contemporary database systems provide a three-level hierarchy for naming relations: catalogs, schemas, and SQL objects such as relations and views. Each user has a default catalog and schema, and the combination is unique to the user. Different applications and users can work independently without worrying about name clashes.

```catalog5.univ schema.course
```

The default catalog and schema are part of an SQL environment that is set up for each connection. We can create and drop schemas by means of create schema and drop schema statements. In most database systems, schemas are created automatically when user accounts are created. The schema name is set to the user account name, and it becomes the default schema for the user account. However, creation and dropping of catalogs is implementation-dependent and not part of the SQL standard.

### Authorization

Amidst the labyrinthine universe of database management, Authorization looms large as a fundamental pillar upon which the entire infrastructure of access control rests. At its core, Authorization governs the granting of privileges to users for accessing, inserting, updating, or deleting data - each of which is deemed a distinct privilege. These authorizations can be bestowed upon a user for a particular part of a database, such as a relation or a view, in combination or exclusively, according to the need of the hour.

However, the database system must ensure that each query or update that is submitted by the user is first checked against the granted authorizations, and if found unauthorized, is promptly rejected. It is not only data authorizations but also schema authorizations that can be granted, providing users with the ability to create, modify or delete relations, amongst other functionalities. Furthermore, a user with some form of authorization can also bestow or revoke privileges to other users as deemed necessary.

Amidst the broad tapestry of Authorization lies the all-encompassing and ultimate authority vested in the hands of the Database Administrator. With a sweeping range of permissions, the Database Administrator is granted the power to create new users, restructure the database, and wield control over the entire infrastructure with utmost finesse, much akin to the authority of a superuser, administrator, or operator for an operating system.

The SQL standard is no stranger to privilege authorization, featuring select, insert, update, and delete privileges as the norm. In a single command, a user can grant all available privileges using the convenient shorthand of 'all privileges'. Whenever a new relation is created, the creator is automatically given all privileges on that relation, providing seamless integration into the system.

Authorization conferral is done through the use of the grant statement in the SQL data-definition language. The basic format of the statement includes a privilege list, a relation or view name, and the intended recipient user or role list. Roles are expounded on further in the subsequent section.

Select authorization is required for the reading of tuples in a relation. For example, granting Amit and Satoshi select authorization on the department relation allows them to read its tuples.

```grant < privilege list >
on <relation name or view name>
to <user/role list>;
```

```grant select on department to Amit, Satoshi;
```

Update authorization on a relation is granted on all attributes of the relation or on only a specific few, determined by the inclusion of the list of attributes in the grant statement. Using the grant statement, a user can give Amit and Satoshi update authorization only on the budget attribute of the department relation.

```grant update (budget) on department to Amit, Satoshi;
```

Insert authorization permits users to insert tuples into a relation while deleting authorization grants users the ability to remove tuples. The 'public' user designation refers to all present and future users of the system, so granting privileges to the public confers those privileges to all users.

```revoke < privilege list >
        on <relation name or view name> from <user/role list>;
```

```revoke select on department from Amit, Satoshi;
revoke update (budget) on department from Amit, Satoshi;
```

Although the SQL authorization mechanism allows for the granting of privileges on a relation or attributes of a relation, it does not permit authorizations on specific tuples. In order to revoke an authorization, a user may use the revoke statement, which follows the same basic format as the grant. However, revocation of privileges can become complicated if the user receiving the revocation has granted the same privilege to another user. Further details on this issue are explored in the following section.

The crucial importance of authorizations and access control becomes increasingly clear. In particular, the notion of roles has emerged as a powerful and elegant means of granting privileges to users in a more efficient and secure manner.

In a university setting, for instance, a variety of individuals may require access to various aspects of the database, such as instructors, teaching assistants, students, deans, and department chairs. Rather than having to manually assign authorizations to each individual user, roles can be created that encapsulate these privileges and be granted to users accordingly. This not only simplifies the administrative process but also minimizes the risk of security breaches by allowing for more granular control over who can access what.

Roles can be created and managed using SQL commands, such as the creation of a role with the "Create role" statement or the granting of privileges to a role with the "grant" statement. Moreover, the privileges of a user or role are not limited solely to those explicitly granted to them; they also inherit any privileges granted to roles that have been granted to them, creating a chain of permissions that can be managed and controlled at multiple levels.

```create role instructor;
        grant select on takes
        to instructor;
                grant dean to Amit; 
        create role dean; 
                grant instructor to dean; 
                grant dean to Satoshi;
```

In short, the use of roles in access control is a versatile and essential tool in the arsenal of any database administrator, one that empowers them to grant and revoke privileges in a more efficient and secure manner.

In the realm of database management, authorization on views is a critical concern, as exemplified by a hypothetical scenario in which a staff member requires access to the salaries of faculty members in the Geology department, but is not authorized to view data pertaining to other departments. To address this issue, a view is created, aptly named "geo instructor", that allows for access to only the necessary data while restricting access to sensitive information. However, before processing any queries, the system must first verify that the user is authorized to access the requested data.

```create view geo instructor as
    (select * 
        from instructor 
        where dept name = ’Geology’);
```

```select *
from geo instructor;
```

It is worth noting that creating a view does not automatically grant the creator all privileges on that view. In fact, the creator only receives privileges that do not exceed their existing authorization. For example, a user cannot be granted update authorization on a view without having update authorization on the underlying relations that were used to define the view. If a view is created on which no authorization can be granted, the system will deny the view creation request.

```grant references (dept name) on department to Mariano;
grant select on department to Amit with grant option;
```

The creation of functions and procedures, which can contain queries and updates, is also supported by SQL. By default, such functions and procedures inherit all the privileges of their creator, but this can be modified using the "SQL security invoker" clause introduced in SQL:2003. This clause allows for the execution of functions and procedures under the privileges of the user who invokes them, as opposed to the privileges of the creator. This capability facilitates the creation of libraries of functions that can be executed under the same authorization as the invoker, enabling greater flexibility and security in database management.

```revoke grant option for select on department from Amit;
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

```{
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

```PreparedStatement pStmt = conn.prepareStatement( "
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

```select * from instructor where name = ’X\’ or \’Y\’ = \’Y’
```

To execute a prepared statement, which is a SQL statement with one or more parameters, the program can use an instance of the class PreparedStatement. In the example provided, a PreparedStatement object is created and used to insert tuples into the instructor relation. The setString and setInt methods are used to set the parameter values before executing the update using the executeUpdate method.

Java Database Connectivity (JDBC) provides a robust and flexible way to connect Java applications to databases. One notable feature of JDBC is the CallableStatement interface, which enables the invocation of SQL-stored procedures and functions. CallableStatement, similar to PreparedStatement for queries, allows for the use of functions and procedures in Java applications. By registering out parameters with the registerOutParameter() method, we can retrieve the data types of function return values and procedure out parameters with the get methods. This functionality provides Java applications with an easy way to interact with databases using stored procedures and functions.

```ResultSetMetaData rsmd = rs.getMetaData();
        for(int i = 1; i <= rsmd.getColumnCount(); i++) {
                System.out.println(rsmd.getColumnName(i)); 
                System.out.println(rsmd.getColumnTypeName(i));
}
```

Furthermore, JDBC's metadata features provide Java programs with the means to retrieve metadata about the database at runtime. This approach makes Java applications more robust to changes in the database schema. The ResultSet interface's getMetaData() method returns a ResultSetMetaData object containing metadata about the result set, which includes information such as the number of columns and the name and type of each column. The DatabaseMetaData interface provides even more metadata about the database system, allowing Java applications to obtain information such as product names, version numbers, and supported features.

```DatabaseMetaData dbmd = conn.getMetaData();
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

```void ODBCexample()
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

```EXEC SQL < embedded SQL statement >;
```

To use embedded SQL, a program must be processed by a preprocessor prior to compilation. This preprocessor replaces embedded SQL requests with host-language declarations and procedure calls that allow for runtime execution of database accesses. Unlike JDBC or ODBC, where SQL statements are interpreted at runtime, some SQL-related errors can be caught at compile time when using embedded SQL.

The EXEC SQL statement is used to identify embedded SQL requests to the preprocessor, and the SQL INCLUDE SQLCA statement is used to identify the place where the preprocessor should insert special variables used for communication between the program and the database system. Before executing any SQL statements, the program must connect to the database using the EXEC SQL and connect to the server using a username using a password statement.

```EXEC SQL BEGIN DECLARE SECTION;
int credit amount;
EXEC SQL END DECLARE SECTION;
```

Variables of the host language can be used within embedded SQL statements but must be preceded by a colon (:) to distinguish them from SQL variables. Embedded SQL statements are similar in form to regular SQL statements but have several important differences. To write a relational query, we use the declare cursor statement, which creates a cursor for the query. The program must use the open and fetch statements to obtain the result tuples.

```EXEC SQL
        declare c cursor for 
        select ID, name 
        from student 
        where tot cred > :credit amount;
```

A single fetch request returns only one tuple, so the program must contain a loop to iterate over all tuples. Embedded SQL assists the programmer in managing this iteration, as the cursor is set to point to the first tuple of the result when the program executes an open statement on a cursor. Each time it executes a fetch statement, the cursor is updated to point to the next tuple of the result. The close statement is used to tell the database system to delete the temporary relation that held the result of the query.

Embedded SQL expressions for database modification do not return a result and are somewhat simpler to express. A database modification request takes the form EXEC SQL . Overall, embedded SQL is a powerful tool for accessing and manipulating database systems, and its use can improve the efficiency and reliability of database operations.

```EXEC SQL < any valid update, insert, or delete>;
```

### Functions and Procedures

While the language comes with a number of pre-built functions, developers can also create their own specialized functions and procedures, store them in the database, and call them from SQL statements. With these custom functions, developers can add business logic to their databases, such as rules for how many courses a student can take in a given semester or how many majors they can be enrolled in.

But the benefits of custom functions don't stop there. Functions can also be used with specialized data types, such as images and geometric objects, where they can perform tasks like checking whether two line segments overlap or comparing two images for similarity. And by storing these functions within the database, developers can ensure that multiple applications have access to them and can change the business rules in one central location without needing to modify other parts of their application.

```create function dept count(dept name varchar(20))
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

```create function instructors of (dept name varchar(20)) returns table (
        ID varchar (5), 
                name varchar (20), dept name varchar (20), salary numeric (8,2))
                return table
                (select ID, name, dept name, salary 
                from instructor 
                where instructor.dept name = instructor of.dept name);
```

Variables are declared using a declare statement, and SQL's support for almost all conditional statements makes it an extremely flexible language. From while statements to repeat statements and conditional statements like if-then-else, SQL's flexibility is unparalleled.

```        if boolean expression
                then statement or compound statement 
        elseif boolean expression 
                then statement or compound statement 
        else statement or compound statement 
        end if
```

In summary, SQL's PSM provides an incredible suite of tools that give it the power of a general-purpose programming language. With its support for functions and procedures, SQL provides great flexibility in developing applications. Its vast range of language constructs allows developers to write complex code that can handle almost any scenario.

SQL allows for functions to be defined in languages like Java, C#, C, or C++. These functions can be more efficient than SQL-defined functions and can perform computations that SQL cannot. However, external language procedures and functions must handle null values in parameters and return values, communicate failure/success status, and deal with exceptions. The exact mechanisms for handling these situations depend on the database system used.

```create procedure dept count proc( in dept name varchar(20),
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

```create trigger timeslot check1 after insert on section
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

```create trigger reorder after update of amount on inventory
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

```select course id, sec id, semester, year, count(ID) as total students
from takes 
group by course id, sec id, semester, year;
```

In addition to these issues, triggers can also cause problems when loading data from backup copies or replicating database updates on backup sites. In such cases, triggers may execute the triggered action more than once, which can lead to an infinite chain of triggering. As a result, database systems may limit the length of such chains or flag them as an error.

Despite these challenges, triggers remain a useful tool in many cases. However, they should be written with great care to avoid errors and complications. When possible, alternative techniques such as stored procedures should be considered instead. Ultimately, the choice of whether or not to use triggers depends on the specific needs and circumstances of the database in question.

![43](https://user-images.githubusercontent.com/124214430/228470686-6953c7a5-f98b-4d02-aca2-59014977ce32.png)

### Recursive Queries**

"findAllPrereqs(cid)" take the course id of the course as a parameter (cid), computes the set of all direct and indirect prerequisites of that course, and returns the set. The function uses three temporary tables: c_prereq, new_c_prereq, and temp. The repeat loop then adds all courses in the new_c_prereq table to the c_prereq table. Next, it computes the prerequisites of all those courses in new_c_prereq, except those that have already been found to be prerequisites of cid, and stores them in the temporary table temp. Finally, it replaces the contents of new_c_prereq by the contents of temp. The repeat loop continues until it finds no new (indirect) prerequisites.

It is worth noting that the use of the except clause in the function ensures that the function works even in the (abnormal) case where there is a cycle of prerequisites. This is particularly useful as cycles are possible in other applications. For example, in relation to "flights(to, from)" which says which cities can be reached from which other cities by a direct flight, the function can be adapted to find all cities that are reachable by a sequence of one or more flights.

```create function ﬁndAllPrereqs(cid varchar(8))
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

```with recursive c prereq(course id, prereq id) as (
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

```select ID, rank() over (order by (GPA) desc) as s rank
from student grades;
```

It is important to note that the order of tuples in the output is not defined, so they may not be sorted by rank. An extra order by clause is required to get them in sorted order. The rank function gives the same rank to all tuples that are equal on the order by attributes. In contrast, the dense rank function does not create gaps in the ordering. It assigns the same rank to tuples with the same GPA and increments the rank for the next unique GPA value.

Ranking can also be performed within partitions of the data. For example, if we want to rank students by department rather than across the entire university, we can use the partition by clause. The following query gives the rank of students within each department:

```select ID, dept name,
        rank () over (partition by dept name order by GPA desc) as dept rank 
from dept grades 
order by dept name, dept rank;
```

Multiple rank expressions can be used within a single select statement. Moreover, when ranking (possibly with partitioning) occurs along with a group by clause, the group by clause is applied first, and partitioning and ranking are done on the results of the group by. This allows users to obtain aggregate values that can then be used for ranking.

While SQL's ranking functions can be used to find the top n tuples by embedding a ranking query within an outer-level query, several database systems provide nonstandard SQL extensions that simplify the job of the optimizer. For instance, some databases allow a clause limit n to be added at the end of an SQL query to specify that only the first n tuples should be output.

SQL's ranking feature is an innovative addition to its suite of tools that offers users a simple and efficient way to perform complex tasks. By leveraging SQL's ranking functions, users can easily rank their data based on various criteria, making data analysis a breeze.

The concept of windowing in databases is a powerful tool for computing aggregate functions over ranges of tuples. By specifying a window, which may overlap with other windows, one can compute aggregate values for specific time intervals, as well as analyze trends in various data sets.

One practical use of windowing is in trend analysis, such as analyzing sales figures or stock market trends. While it is relatively straightforward to compute aggregates over a fixed window of time, such as a 3-day period, it becomes more challenging to do so for every 3-day period. This is where the windowing feature of SQL comes in handy.

```select year, avg(num credits)
        over (order by year rows 3 preceding) 
        as avg total credits 
from tot credits;
```

SQL allows for the computation of aggregate values over specific windows by using the "rows preceding" or "rows following" syntax. For example, a query could be written to compute the average number of credits taken by students over the previous three years, sorted by year. Additionally, the "range between" syntax can be used to specify a range based on the value of the order attribute.

```select year, avg(num credits)
        over (order by year rows unbounded preceding) 
        as avg total credits 
from tot credits;

```

```select year, avg(num credits)
        over (order by year rows between 3 preceding and 2 following) 
        as avg total credits 
from tot credits;
```

Furthermore, windowing can be used to partition data by specific attributes, such as department names, in order to compute aggregate values for each subset of data. This is done by including a "partition by" clause in the SQL query.

```select dept name, year, avg(num credits)
        over (partition by dept name 
                order by year rows between 3 preceding and current row)
        as avg total credits 
from tot credits dept;
```

Overall, the windowing feature in SQL provides a powerful tool for analyzing trends and computing aggregate values over specific windows of data. Its flexibility and ease of use make it an essential tool for data analysis and decision-making in a wide variety of fields.

### OLAP**

The art of data analysis has come a long way since the days of spreadsheet applications. In today's world, businesses are looking for more sophisticated ways to make sense of their vast amounts of data. Enter the online analytical processing (OLAP) system, a revolutionary tool that allows analysts to view summaries of multidimensional data in an interactive and speedy fashion.

```sales (item name, color, clothes size, quantity)
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

```select *
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

```select decode(grouping(item name), 1, ’all’, item name) as item name
                decode(grouping(color), 1, ’all’, color) as color 
                sum(quantity) as quantity 
                from sales 
                group by cube(item name, color);
```

In addition to the decode function, the rollup construct has also been discussed. Similar to the cube construct, rollup generates fewer groups by queries and can be useful for hierarchies when groups are of frequent practical interest.

```select item name, color, clothes size, sum(quantity)
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

In the realm of relational algebra, a crucial task is to assign a name to the results of expressions, as unlike database relations, they lack a distinct identifier. Fortunately, the rename operator, symbolized by the lowercase Greek letter rho, offers a means to do just that. Given a relational algebra expression E, the operator rx(E) generates the outcome of expression E under the name x. Interestingly, a relation r is also considered a trivial relational algebra expression, and thus the rename operation can be applied to r to obtain the same relation under a new name.

Another form of the rename operation involves an expression E with arity n. In this case, rx(A1,A2,...,An)(E) yields the result of E under the name x and with the attributes renamed to A1, A2,..., An. An example of renaming a relation involves the query "Find the highest salary in the university." Our strategy involves computing a temporary relation of non-maximum salaries and then taking the set difference between the rsalary(instructor) relation and the temporary relation to obtaining the desired outcome.

![Figure 64 - Result of the subexpressiont](64.png)

To compute the temporary relation, a mechanism to differentiate between two salary attributes is necessary. The rename operation comes to the rescue, enabling one reference to the instructor relation to be renamed, permitting the relation to be referenced twice without ambiguity. The temporary relation comprises salaries that are not the largest, and the resulting expression is given by:

```Ninstructor.salary(Qinstructor.salary < d.salary(instructor × pd(instructor)))

To find the highest salary in the university, the expression:

Nsalary(instructor) −
Ninstructor.salary(instructor.salary < d.salary(instructor × Rd(instructor)))
```

![Figure 65 - Highest salary in the university](65.png)

is employed. The rename operation is not obligatory, as positional notation can be used instead to refer to attributes of a relation. Here, $1, $2,... refer to the first, second, and subsequent attributes. While this notation can also be applied to the results of relational-algebra operations, it is often cumbersome and inconvenient for humans to use. As such, we avoid it in this textbook.

As we delve deeper into the fundamentals of relational algebra, we find that a basic expression in this realm consists of either a relation in the database or a constant relation that is explicitly stated. The latter is represented by listing the tuples within braces, much like a set. For instance, a constant relation would appear as { (22222, Einstein, Physics, 95000), (76543, Singh, Finance, 80000) }.

![Figure 66 - Courses offered in both the Fall 2009 and Spring 2010 semesters](66.png)

To construct a general expression in relational algebra, we utilize smaller sub-expressions. Two relational-algebra expressions, E1 and E2, can be used to construct a range of relational-algebra expressions, including union, difference, cross-product, selection with a predicate, projection with a list of attributes, and renaming.

Although the fundamental operations of relational algebra are powerful enough to address any relational algebra query, we encounter some queries that become lengthy to express. Therefore, we define additional operations that, while not adding any power to the algebra, simplify common queries. Each new operation is given with an equivalent expression that uses only the fundamental operations.

One of these new operations is a set intersection, denoted by the symbol "∩". By utilizing set intersection, we can write simpler queries for finding the set of all courses taught in both the Fall 2009 and the Spring 2010 semesters, as well as for other similar cases. Interestingly, any relational-algebra expression that uses a set intersection can be rewritten using a pair of set-difference operations.

```Pcourse id (Qsemester = “Fall” ∧ year=2009 (section)) ∩
Pcourse id (Qsemester = “Spring” ∧ year=2010 (section))
```

Another new operation is the natural join, denoted by the symbol "⨝". This operation allows us to combine certain selections and a Cartesian product into one operation. The natural-join operation forms a Cartesian product of its two arguments, performs selection-forcing equality on those attributes that appear in both relation schemas and removes duplicate attributes. The resulting relation is smaller and contains only those tuples that give information about an instructor and a course that the instructor actually teaches. The natural join is an essential operation that simplifies many queries involving Cartesian products.

The relational-algebraic expression, in all its elegance, can be made even more palatable through the use of the assignment operation. This operation, denoted by the symbol ←, enables the parts of the expression to be assigned to temporary relation variables for the sake of convenience. In a manner akin to assignment in a programming language, the result of the expression to the right of the ← is assigned to the relation variable on the left of the ←, with no relation being displayed to the user. The beauty of this approach lies in its ability to create a sequential program of assignments followed by an expression that displays the value of the query's result. It is important to note that assignments in relational algebra queries must always be made to a temporary relation variable, as assignments to permanent relations constitute a modification of the database. Though it does not add any additional power to the algebra, the assignment operation remains a valuable tool for expressing complex queries with ease.

The outer-join operation proves to be a vital extension of the join operation by catering to instances of missing information. When tuples in either of the relations being joined are not part of the join's result due to non-matching, the outer join operation comes to the rescue. There are three variations of the outer join operation, namely left outer join, right outer join, and full outer join, each with a distinct approach to preserving lost tuples.

The left outer join operation takes all the tuples in the left relation that do not have a matching tuple in the right relation, fills in the attributes from the right relation with null values, and adds these tuples to the natural join result. On the other hand, the right outer join operation pads tuples from the right relation with nulls and adds them to the result of the natural join when there is no match in the left relation. The full outer join operation performs both left and right outer joins, adding tuples from the left relation and the right relation that do not match the result of the join.

It is worth noting that outer-join operations have the potential to generate results containing null values. Thus, it becomes essential to specify how different relational-algebra operations treat null values. However, it is fascinating to observe that outer-join operations can be expressed by the basic relational-algebra operations. For example, the left outer join operation, r x s, can be expressed as (r x s) U (r - PR(r X s)) ×{(null,..., null)}, where the constant relation {(null,..., null)} is on the schema S - R. Overall, the outer-join operation plays a pivotal role in preserving lost tuples and filling the gaps in the join operation.

In the realm of relational algebra operations, two extensions provide further functionality that is not possible with the basic set of operations. These are the generalized projection and aggregate operations, which offer the ability to incorporate arithmetic and string functions, as well as aggregate functions such as min and average respectively.

The generalized-projection operation takes an algebraic expression E and a list of arithmetic expressions F1 through Fn that consist of constants and attributes of E and generates a new relationship that includes the projected attributes with any arithmetic operations applied to them. For example, the expression "PID, name, dept name,salary÷12(instructor)" would yield a new relation containing the ID, name, department name, and monthly salary of each instructor.

Aggregate operations, on the other hand, take a collection of values and return a single value based on a given function. Common aggregate functions include sum, average, count, min, and max, and can be applied to multisets of values where duplicates are not eliminated, or to sets of values where duplicates are removed. The calligraphic G symbol denotes the use of aggregation, with a subscript indicating the specific function to be applied. For instance, "Gsum(salary)(instructor)" returns a relation with a single attribute containing the sum of all instructors' salaries.

In addition, aggregation can be applied to groups of sets of tuples, where the resulting relation contains a single row for each group and a column for each attribute. The expression "dept.nameGaverage(salary)(instructor)" groups the tuples in the instructor relation by department name, calculates the average salary for each group and returns a relation with a single row for each department containing the department name and average salary.

![Figure 73 - Tuples of the instructor relation, grouped by the dept name attribute](73.png)

These operations provide further power to the relational-algebra language, enabling more complex queries and analyses to be performed on relational databases.

![Figure 74 - The result relation for the query “Find the average salary in each department”](74.png)

### The Tuple Relational Calculus

To express a query in the tuple relational calculus, we use the notation {t | P(t)}, which represents the set of all tuples t such that predicate P is true for t. By using t[A] to denote the value of tuple t on attribute A, and t ∈ r to denote that tuple t is in relation r, we can write queries such as "Find the ID, name, dept name, salary for instructors whose salary is greater than $80,000" as {t | t ∈ instructor ∧ t[salary] > 80000}.

To express more complex queries, we need to use the "there exists" construct from mathematical logic. For instance, to find the instructor ID for each instructor with a salary greater than $80,000, we use the notation {t |∃ s ∈ instructor (t[ID] = s[ID] ∧ s[salary] > 80000)}, which reads as "The set of all tuples t such that there exists a tuple s in relation instructor for which the values of t and s for the ID attribute are equal, and the value of s for the salary attribute is greater than $80,000."

![Figure 75 - Names of all instructors whose department is in the Watson building](75.png)

Similarly, queries involving multiple relations can be expressed using multiple "there exists" clauses connected by the logical operator "and." For example, to find the names of all instructors whose department is in the Watson building, we can use the notation {t |∃ s ∈ instructor (t[name] = s[name] ∧∃ u ∈ department (u[dept name] = s[dept name] ∧ u[building] = “Watson”))}.

Finally, we can use the logical operator "or" to find the set of all courses taught in the Fall 2009 semester, the Spring 2010 semester, or both. If we want only those course id values for courses that are offered in both the Fall 2009 and Spring 2010 semesters, we simply change the "or" to "and" in the preceding expression.

With these powerful tools at our disposal, we can now tackle more complex queries, such as "Find all the courses taught in the Fall 2009 semester but not in Spring 2010 semester," using the "not" symbol to exclude the courses offered in both semesters. The tuple relational calculus offers a concise and expressive language for querying relational databases, allowing us to uncover insights and patterns hidden in the data.

Tuple-relational calculus is a powerful tool for expressing queries. However, it is not without its limitations. In order to ensure that queries are both meaningful and computable, we must impose certain constraints on their structure.

At the heart of tuple-relational calculus is the concept of a formula, which, takes the form {t|P(t)}. Here, P is a formula consisting of atoms, which can be either relational expressions or comparisons involving tuple variables and constants. Tuple variables may be bound or free, depending on whether they are quantified by a logical operator.

In order to avoid the problem of infinite relations, we must ensure that all expressions are "safe," meaning that their domain (the set of values referenced by the formula) is finite. This is accomplished by imposing restrictions on the structure of the formula, such as disallowing expressions that generate infinite relations.

In the realm of relational databases, the expressive power of languages is a topic of great interest and significance. In particular, the tuple relational calculus, when restricted to safe expressions, has been found to be equally expressive as the basic relational algebra. This equivalence holds for all fundamental relational algebraic operations, including union, difference, cartesian product, selection, and projection. It is important to note that this result excludes extended relational operations, such as generalized projection and aggregation.

Remarkably, every relational algebraic expression that employs only the basic operations has an equivalent expression in the tuple relational calculus. Moreover, the converse is also true, and every tuple-relational-calculus expression has an equivalent relational-algebra expression. While the proof of this equivalence is beyond the scope of our present discussion, we point interested readers to the bibliographic notes for relevant references. Some crucial aspects of the proof are included in the exercises.

Notably, the tuple relational calculus does not have any direct equivalent of the aggregate operation, but it can be extended to support aggregation. Furthermore, extending the tuple relational calculus to handle arithmetic expressions is a straightforward matter. Overall, these findings highlight the rich and flexible nature of relational database languages and the fascinating interplay between different formalisms in this domain.

### The Domain Relational Calculus

Domain Relational Calculus, a prominent method for querying databases, diverges from its sibling, Tuple Relational Calculus, by utilizing domain variables that represent values from an attribute's domain rather than an entire tuple's values. Despite their differences, Domain and Tuple Relational Calculus are closely linked. The former acts as the theoretical foundation for the commonly employed QBE language, while the latter forms the basis of the widely utilized SQL language.

The domain relational calculus is an important tool for expressing queries. This form of calculus uses domain variables that take on values from an attribute's domain, rather than values for an entire tuple. To better understand this calculus, it's helpful to consider its formal definition.

An atom is a formula.
If P1 is a formula, then so are ¬P1 and (P1).
If P1 and P2 are formulae, then so are P1 ∨ P2, P1 ∧ P2,and P1 ⇒ P2.
If P1(x) is formulaic x, where x is a free domain variable, then ∃ x (P1(x)) and ∀ x (P1(x)) are also formulae.
It's worth noting that this calculus serves as the theoretical basis of the popular QBE language, just as relational algebra serves as the basis for SQL. By understanding the formal definition of the domain relational calculus and the rules for building up formulae, one can effectively query databases and retrieve the information they need.

As we delve further into the world of database systems, we encounter a realm where queries reign supreme. In the pursuit of extracting information from databases, it is essential to understand the intricacies of the domain of relational calculus. This calculus, much like its tuple-based counterpart, involves a language for expressing queries over relations. In the pursuit of clarity, we provide examples of domain-relational-calculus queries that mirror those written in tuple calculus, highlighting their similarities.

However, we must note a crucial difference between these two forms of calculus. In tuple calculus, we can readily bind a variable to a relation using the symbol "∈". In contrast, domain calculus does not bind variables to tuples but rather to domain values. This subtlety is significant because the domain of a variable is unconstrained until the subformula "∈ instructor" restricts it to a specific domain.

As we progress in our study, we encounter queries that can result in infinite relations, causing a roadblock to our quest for understanding. Therefore, it is essential to define safety rules to prohibit such expressions. In domain calculus, we must also pay heed to the form of subformulas within "there exists" and "for all" clauses. Our quest for safe expressions leads us to add further restrictions to ensure we can test subformulas without having to consider an infinite number of possibilities.

Thus, in our pursuit of knowledge, we must balance the elegance of calculus with the necessary rules to ensure we can safely extract information from databases.

# DATABASE DESIGN

In a world where information is king, the design and management of database systems are critical to the success of modern enterprises. These systems handle vast amounts of data that are intimately intertwined with the operations of the organization, whether it be for the production of information products or the support of essential devices and services.

The first two chapters of this section delve into the essential building blocks of database schema design. Specifically, Chapter 7 explores the entity-relationship (E-R) model, a high-level data model that identifies and organizes basic objects, or entities, and the relationships between them. This model represents a crucial first step toward developing a comprehensive and effective database schema.

However, relational database design - the creation of a relational schema - is equally important and often more complex. Chapter 8 introduces several "normal forms" that help distinguish well-designed schemas from those that may be prone to inconsistencies and inefficiencies. These forms provide a framework for optimizing query performance while maintaining data integrity.

To design a complete and effective database application environment that meets the needs of a modern enterprise, a host of additional issues must be addressed. Chapter 9 delves into some of the most critical of these topics, including the design of user interfaces and multi-layered system architectures, which form the foundation for large-scale applications. Additionally, the chapter provides a comprehensive exploration of security at both the application and database levels, ensuring that sensitive data is protected from unauthorized access or compromise.

## Database Design and the E-R Model

As we delve deeper into the intricacies of database systems, it becomes imperative to comprehend the nuances of database schema design. In order to effectively capture the essence of the database and its interrelated components, it is crucial to have a solid understanding of the entity-relationship (E-R) model. This model is a potent tool for identifying the entities that are part of the database and the relationships that bind them together.

This chapter elucidates the key concepts of the E-R model, highlighting its significance in relation to a robust database schema design. The crux of the matter is to transform the E-R design into a set of relation schemas and to capture the constraints that govern those relations. The next chapter deals with the analysis of the set of relation schemas, using a broader range of constraints to determine whether it is a good or bad database design.

It is imperative that one has a solid understanding of the fundamental principles of database design. These two chapters not only provide a comprehensive overview of the process but also equip the reader with the necessary knowledge to create a robust and effective database schema design.

### Overview of the Design Process

In the complex and multifaceted task of creating a database application, the needs of users take center stage. This entails designing the database schema, as well as the programs that access and update the data, and a security scheme to regulate access. In this chapter, the focus is on the design of the database schema, while also briefly outlining some of the other tasks that lie ahead.

To design a complete database application environment that meets the needs of the enterprise being modeled, one must be attuned to a wide range of issues. These issues have a bearing on various design choices at the physical, logical, and view levels. Therefore, attention must be paid to these aspects of the expected use of the database in order to create an effective and comprehensive design.

The process of designing a database application is an intricate and multifaceted task that involves various phases. While creating a small-scale application may allow for a straightforward approach to designing the database schema, real-world applications are far more complex and necessitate extensive interaction between the database designer and application users to understand and represent the data requirements of the enterprise being modeled. The first phase of database design involves characterizing the data needs of the prospective database users, which entails interacting extensively with domain experts and users to obtain a comprehensive specification of user requirements.

Once the user requirements are established, the designer then selects a data model and translates these requirements into a conceptual schema of the database. The entity-relationship model is a common method for representing the conceptual design, which specifies the entities, attributes, relationships, and constraints of the database. At this stage, the designer's focus is on describing the data and their relationships, rather than specifying physical storage details.

The conceptual schema also indicates the functional requirements of the enterprise, which describe the operations or transactions that will be performed on the data. The next phase involves mapping the high-level conceptual data model to a logical data model, typically the relational data model, and mapping the conceptual schema defined using the entity-relationship model into a relation schema. Finally, the resulting system-specific database schema is used in the physical-design phase, which specifies the physical features of the database, including the form of file organization and choice of index structures.

It is crucial to design the database schema with care, as changes to the logical schema may affect a number of queries and updates scattered across application code. The physical schema can be changed relatively easily after an application has been built, but logical schema changes require greater effort and should be avoided if possible. Therefore, the database design phase should be conducted thoroughly before building the rest of the database application to ensure that all data requirements are satisfied and redundant features are removed.

The art of designing a database schema is not to be underestimated, as it requires careful consideration of the many entities and relationships within an enterprise. These entities must be identified and represented in the design, with each one related to the others in a way that captures the complexity of the enterprise. However, in doing so, we must be wary of two major pitfalls that can lead to poor design: redundancy and incompleteness.

Redundancy occurs when information is needlessly repeated, leading to potential inconsistencies if updates are not made uniformly. For example, if we store the course identifier and title with each course offering, we redundantly store the title with every offering. Instead, it suffices to store only the identifier with each offering and associate the title with the identifier in a course entity. Incompleteness, on the other hand, occurs when certain aspects of the enterprise cannot be modeled due to inadequate design. If we only have entities corresponding to course offerings and not to courses themselves, we cannot represent information about a new course unless it is already being offered. This leads to problematic design and workarounds that are often unattractive and impractical.

Avoiding bad designs is just the beginning, however. There may be a plethora of good designs to choose from, each with its own set of trade-offs. For instance, when a customer buys a product, is the sale itself a relationship between the customer and the product, or is the sale an entity that relates to both the customer and the product? The choice made here can have important implications for the overall design.

Ultimately, database design is a challenging problem that requires both scientific and artistic sensibilities. It is a task that demands a deep understanding of the enterprise being modeled, as well as an appreciation for the elegance and simplicity of good design.

### The Entity-Relationship Model

The Entity-Relationship (E-R) data model is a powerful tool in the field of database design. Its purpose is to provide a clear and concise representation of the logical structure of a database by mapping real-world entities and relationships onto a conceptual schema. This has made it a widely-used and popular approach for database design.

The E-R data model is based on three fundamental concepts: entity sets, relationship sets, and attributes. These concepts allow for the creation of a comprehensive schema that accurately represents the interactions and meanings of an enterprise. In addition, the E-R model has a graphical representation, the E-R diagram, which helps designers visualize the structure of the database.

The E-R data model has revolutionized the field of database design, providing a powerful framework for accurately representing complex relationships and entities in a logical and efficient manner. Its widespread use is a testament to its effectiveness and usefulness in the field.

The entity-relationship (E-R) data model is an invaluable tool for creating a conceptual schema that accurately maps the interactions of real-world enterprises. Comprised of three core concepts, namely entity sets, relationship sets, and attributes, the E-R model is a powerful framework for designing databases. In particular, entity sets represent distinct "things" or "objects" in the real world that can be identified by a set of properties, or attributes. Whether concrete (e.g. people or books) or abstract (e.g. courses or reservations), entity sets share the same attributes and is grouped into collections, or extensions.

For instance, a university database may include the entity sets of instructors and students, with attributes such as ID, name, department, and salary for instructors, and ID, name, major, and GPA for students. These entity sets need not be disjoint; a person can be both an instructor and a student, or neither. Attributes describe the properties possessed by each member of an entity set, with each entity having its own unique value for each attribute. The ID attribute is typically used to uniquely identify entities within a set, and databases consist of a collection of entity sets that may include dozens of distinct collections.

Ultimately, the entity-relationship model is a powerful tool for conceptualizing complex databases and designing schema that accurately reflects the interactions of real-world enterprises. Through the use of entity sets, attributes, and relationship sets, database designers can create an intuitive and robust data model that captures the essence of complex data structures.

![Figure 76 -  Entity sets instructor and student](75.png)

The notion of a relationship takes center stage. A relationship is a connection between several entities that helps to make sense of the data being modeled. At its core, a relationship is a mathematical relation on n ≥ 2 (possibly nondistinct) entity sets. When multiple relationships of the same type exist, they can be grouped together as a relationship set.

![Figure 77 -  Relationship set advisor](76.png)

Consider, for example, the two entity sets of instructor and student, which can be linked together through a relationship set called advisor. This relationship set captures the connection between a specific instructor and a specific student, thus formalizing the advisory role of the instructor to the student. Similarly, a relationship set takes can link the entity sets of students and sections to represent the enrollment of students in specific course sections.

The concept of participation plays a critical role in relationship sets. This refers to the involvement of entity sets in the relationship set. Each entity set plays a role in the relationship, which helps clarify the meaning of the relationship. In cases where the entity sets in the relationship set are not distinct, explicit role names are necessary to specify how the entity participates in a relationship instance.

Descriptive attributes can also be associated with relationships, such as the date an instructor became an advisor to a student. A relationship instance must be uniquely identifiable from its participating entities, without the use of descriptive attributes.

![Figure 78 -  Date as attribute of the advisor relationship set](77.png)

In many cases, multiple relationship sets involving the same entity sets can exist. Binary relationship sets are the most common, but there are cases where a relationship set may involve more than two entity sets. The modeling of relationships in database systems is a complex task, but a crucial one for creating accurate and useful databases.

In the realm of database design, the attributes of an entity set play a crucial role in representing real-world objects and their characteristics. In the context of the E-R model, each attribute is associated with a domain of permitted values, which defines the set of valid values for that attribute. For example, the domain of the "course id" attribute might be a set of text strings of a particular length, while the domain of the "semester" attribute might be a set of strings from the set {Fall, Winter, Spring, Summer}.

In the E-R model, an attribute is a function that maps from an entity set into a domain, allowing each entity to be described by a set of (attribute, data value) pairs. These pairs represent the values of each attribute for a given entity, providing a significant portion of the data stored in the database.

Attributes in the E-R model can be characterized by several types, including simple and composite attributes, single-valued and multivalued attributes, and derived attributes. Simple attributes represent indivisible, atomic values, while composite attributes can be divided into subparts. Single-valued attributes have a single value for each entity, while multivalued attributes can have a set of values for a specific entity. Derived attributes can be derived from other attributes or entities, with the value being computed when required.

![Figure 79 -  Composite attributes instructor name and address](78.png)

An attribute can also take a null value, indicating that the entity does not have a value for that attribute. Null values can signify "not applicable" or "unknown," and they play an important role in handling missing or incomplete data.

Overall, the attributes of an entity set provide a rich and nuanced representation of the characteristics of real-world objects, enabling powerful database modeling and analysis capabilities.

### Constraints

Constraints play a crucial role in ensuring data integrity and consistency. An essential aspect of constraints is mapping cardinalities, which express the relationship between entities in a database. While mapping cardinalities are most commonly used for binary relationship sets, they can also apply to more complex relationship sets involving multiple entity sets.

For a binary relationship set, the mapping cardinality can be classified as one-to-one, one-to-many, many-to-one, or many-to-many. The choice of mapping cardinality depends on the specific real-world situation that the relationship set represents. Take, for example, the advisor relationship set in a university. If a student can only be advised by one instructor, and an instructor can advise several students, then the relationship set from instructor to student is one-to-many. On the other hand, if a student can be advised by multiple instructors, as is the case with joint advising, the relationship set becomes many-to-many.

![Figure 80 -  Mapping cardinalities. (a) One-to-one. (b) One-to-many](79.png)

![Figure 81 -  Mapping cardinalities. (a) Many-to-one. (b) Many-to-many](80.png)

Mapping cardinalities are a powerful tool for designing databases that accurately reflect the relationships between entities in the real world. By understanding mapping cardinalities, designers can ensure that their databases maintain data integrity and consistency, allowing for more accurate and efficient data processing.

The art of database design involves more than just defining entities and their relationships. One key aspect is setting constraints to ensure that the contents of the database adhere to certain standards. In this vein, mapping cardinalities and participation constraints serve as powerful tools to govern relationships among entity sets.

Mapping cardinalities are ratios that describe how many entities can be associated with another entity through a relationship set. While binary relationship sets are the most amenable to mapping cardinalities, they can also be applied to more complex sets involving more than two entity sets. For binary relationship sets, four mapping cardinalities exist one-to-one, one-to-many, many-to-one, and many-to-many. The choice of which mapping cardinality to use depends on the particulars of the real-world scenario being modeled.

Participation constraints, on the other hand, refer to the degree to which an entity set participates in a relationship set. If every entity in an entity set participates in at least one relationship in a relationship set, the participation is total. If only some entities in the entity set participate, the participation is partial. For instance, in the advisor relationship set, we would expect every student entity to have at least one corresponding instructor entity, making the participation total for students. In contrast, instructors need not advise any students, rendering participation partial for instructors. By setting participation constraints, database designers can ensure data consistency and reduce the risk of data corruption.

The ability to distinguish entities from one another is of paramount importance. Entities may seem distinct on a conceptual level, but from a database perspective, it is crucial to express their differences in terms of their attributes. To this end, we require a set of attribute values that can uniquely identify each entity. Thus, the notion of a key, as previously defined for relation schemas, applies to entity sets as well.

A key for an entity is a set of attributes that can distinguish one entity from another. The concepts of superkey, candidate key, and primary key, which are fundamental to relation schemas, are also applicable to entity sets. Keys are essential to identifying relationships uniquely, and thereby distinguishing one relationship from another.

For instance, let us consider a relationship set R, involving entity sets E1, E2,..., En. If primary-key(Ei) denotes the set of attributes that form the primary key for entity set Ei, then the composition of the primary key for relationship set R is determined by the set of attributes associated with R. If R has no attributes associated with it, then the set of attributes primary-key(E1) ∪ primary-key(E2) ∪··· ∪ primary-key(En) describes a unique relationship in set R.

On the other hand, if R has attributes a1, a2,..., am associated with it, then the set of attributes primary-key(E1) ∪ primary-key(E2) ∪··· ∪ primary-key(En) ∪{a1, a2,..., am} describes an individual relationship in set R. In both of the above cases, the set of attributes primary-key(E1) ∪ primary-key(E2) ∪··· ∪ primary-key(En) forms a superkey for the relationship set.

However, if the attribute names of primary keys are not unique across entity sets, they are renamed to distinguish them. If an entity set participates more than once in a relationship set, the role name is used instead of the name of the entity set to form a unique attribute name.

The structure of the primary key for the relationship set is determined by the mapping cardinality of the relationship set. The primary key of advisor, a relationship set involving entity sets instructor and student with attribute date, is the union of the primary keys of instructor and student if the relationship set is many-to-many. If the relationship is many-to-one from student to instructor, then the primary key of the advisor is simply the primary key of the student. Similarly, if an instructor can advise only one student, then the primary key of the advisor is simply the primary key of the instructor. For one-to-one relationships, either candidate key can be used as the primary key.

While the choice of the primary key for non-binary relationships is straightforward when no cardinality constraints are present, it becomes more complicated in the presence of such constraints. However, as we have not yet discussed how to specify cardinality constraints on non-binary relationships, we defer this discussion to later chapters.

### Removing Redundant Attributes in Entity Sets

In designing a database using the E-R model, selecting the appropriate entity sets and their corresponding attributes is crucial. The choice of attributes lies in the hands of the designer, who possesses a good understanding of the structure of the enterprise. However, the relationship sets among various entities may result in redundant attributes, which should be removed from the original entity sets.

For instance, consider the entity sets instructor and department. Both contain the attribute dept name, with the dept name serving as the primary key for the department entity set. Therefore, the dept name is redundant in the instructor entity set and should be removed. While this may appear counterintuitive, treating the connection between instructors and departments uniformly as a relationship makes the logical relationship explicit and avoids premature assumptions.

Similarly, the student entity set is related to the department entity set through the relationship set student dept, eliminating the need for a dept name attribute in the student entity set. Another example involves the entity sets section and time slot, which share the attribute time slot id. Since time slot id is the primary key for the entity set time slot, it is redundant in the entity set section and should be removed.

Finally, redundant attributes can also exist within the same entity set. For instance, the entity set section contains the attributes building and room number, which are also present in the related entity set classroom. Thus, these attributes are redundant and should be removed from the section entity set.

By avoiding redundant attributes in entity-relationship design, we can create a streamlined and efficient database. For the university example discussed in this article, a comprehensive list of entity sets and relationship sets has been provided, showcasing a well-designed database free of redundant attributes.

### Entity-Relationship Diagrams

Entity-Relationship Diagrams (ERDs) are graphical representations of the logical structure of a database that utilize simple and clear components to achieve widespread usage. ERDs consist of entity sets, relationship sets, and attributes, which are linked together by lines and arrows to specify the nature of the relationships between entities.

![Figure 82 -  E-R diagram corresponding to instructors and students](81.png)

By mapping cardinality, ERDs can further indicate the number of times each entity participates in relationships within a relationship set. It is important to note that the placement of arrows in a relationship set indicates the nature of the relationship between the entity sets. One-to-one, one-to-many, many-to-one, or many-to-many relationships can be represented with either a directed or undirected line, depending on the cardinality. ERDs can also specify minimum and maximum cardinalities, with minimum values of 1 indicating total participation, maximum values of 1 indicating at most one relationship, and maximum values of * indicating no limit.

![Figure 83 -  E-R diagram with an attribute attached to a relationship set](82.png)

![Figure 84 -  Relationships. (a) One-to-one. (b) One-to-many. (c) Many-to-many](83.png)

Overall, ERDs provide a useful tool for visualizing and designing complex databases.

To aid in understanding this concept, a visual representation of composite attributes in the E-R notation is. Here, the attribute "instructor" is replaced by the composite attribute "name", which consists of three component attributes: first name, middle initial, and last name.

Another example is given in the case of adding an address attribute to the instructor entity set. The composite attribute "address" is defined, as consisting of four component attributes: street, city, state, and zip code. Further complexity arises as the street attribute itself is a composite attribute, comprised of three component attributes: street number, street name, and apartment number.

![Figure 85 -  Cardinality limits on relationship sets](84.png)

As if this wasn't enough, the figure above also depicts two other attribute types: multivalued and derived attributes. The former, denoted by "{phone number}", indicates an attribute that can have multiple values for a single entity. The latter, represented by "age()", is an attribute that is not stored in the database but instead calculated from other attributes.

![Figure 86 -  E-R diagram with composite, multivalued, and derived attributes](85.png)

In E-R diagrams, roles can be identified by marking the lines connecting diamonds to rectangles. The image presented in the figure above demonstrates this approach, where the course entity set and the prereq relationship set are linked by role indicators such as course id and prereq id.

![Figure 87 -  E-R diagram with role indicators](86.png)

![Figure 88 -  E-R diagram with a ternary relationship](87.png)

In the realm of entity-relationship (E-R) diagrams, roles can be designated by the labels attached to lines linking diamonds to rectangles. This is illustrated in the Figure below, where the roles of course id and prereq id are indicated by labels on the line between the course entity set and the prereq relationship set.

Nonbinary relationship sets, which involve more than two entity sets, can also be depicted in E-R diagrams. Figure 7.13 showcases an example involving three entity sets: instructor, student, and project. These sets are interconnected through the proj guide relationship set.

It's worth noting that certain types of many-to-one relationships can be specified in the context of nonbinary relationship sets. For instance, if a student can have no more than one instructor as a project guide, this constraint can be represented by an arrow pointing to the instructor on the edge from proj guide. However, to avoid ambiguity, we allow at most one arrow out of a relationship set, since diagrams with multiple arrows can be interpreted in different ways. We delve into functional dependencies, which provide a means of unambiguously specifying these complex relationships.

In the world of database design, the concept of weak entity sets stands out as a particularly nuanced and intricate topic, one that requires a keen eye for detail and a deep understanding of the interrelationships between data entities. At its core, a weak entity set is an entity set that lacks the necessary attributes to form a primary key, and as such, it must be associated with another entity set, known as the identifying or owner entity set, to derive its unique identity.

To fully appreciate the complexity of this concept, we must delve deeper into the inner workings of weak entity sets. Take, for example, the case of a section entity, which is uniquely identified by a course identifier, semester, year, and section identifier. At first glance, section entities appear to be related to course entities, and so we create a relationship set between section and course entity sets.

However, upon closer inspection, we find that the information in this relationship set is redundant, as the section already has an attribute that identifies the course with which it is related. To address this redundancy, we could simply remove the relationship, but doing so would result in an implicit relationship between section and course, which is not desirable.

Instead, we must find a way to store the necessary information in a more efficient and meaningful way. One option is to remove the course ID attribute from the section entity and only store the remaining attributes. However, this approach presents a new problem, as the section entity would no longer have enough attributes to identify a specific section entity uniquely.

To solve this issue, we treat the relationship between section and course as a special relationship that provides the extra information required to identify section entities uniquely. This is where the concept of the weak entity set comes into play.

A weak entity set is an entity set that lacks sufficient attributes to form a primary key and must be associated with an identifying entity set to derive its unique identity. The identifying entity set is said to own the weak entity set that it identifies, and the relationship associating the two entity sets is known as the identifying relationship.

![Figure 89 -  E-R diagram with a weak entity set](88.png)

In the case of section and course, the course is the identifying entity set for section, and the relationship between the two, known as sec course, is the identifying relationship. The discriminator of a weak entity set is a set of attributes that allows us to distinguish among all the entities in the weak entity set that depend on one particular strong entity.

In the case of the section, the discriminator consists of the attributes sec id, year, and semester. The primary key of a weak entity set is formed by the primary key of the identifying entity set plus the weak entity set's discriminator.

As we can see, the concept of weak entity sets is a nuanced and complex topic that requires a deep understanding of database design principles. However, by mastering this concept, we can create more efficient and meaningful database structures that better represent the relationships between data entities.

In a stunning demonstration of conceptual modeling, the authors present an E-R diagram that encapsulates the intricate workings of a university enterprise. This diagram, which is equivalent to the textual description of the university E-R model presented earlier in the text, is enriched with several additional constraints that underscore the complexity of this domain.

![Figure 90 -  E-R diagram for a university enterprise](89.png)

Of particular note is the constraint that mandates each instructor to have exactly one associated department, which is represented by a double line between instructor and inst dept, indicating total participation of instructor in inst dept. Moreover, the diagram reveals that each instructor can have at most one associated department, as depicted by the arrow from inst dept to department.

Similarly, the course and student entities have double lines to relationship sets course dept and stud dept, respectively, while the section is now a weak entity set, with attributes sec id, semester, and year forming the discriminator. In a masterful stroke of design, the sec course is the identifying relationship set that relates the weak entity set section to the strong entity set course.

Notably, the relationship set takes has a descriptive attribute grade, and each student has at most one advisor. The authors tantalize readers with the promise that, they will unveil how this E-R diagram can be harnessed to derive the various relation schemas used in the enterprise. Truly, a tour de force of conceptual modeling that leaves readers eagerly anticipating what lies ahead.

### Reduction to Relational Schemas

In the world of database design, the E-R model and the relational database model stand out as the most significant and widely used paradigms. While both models are abstract and logical representations of real-world enterprises, they rely on similar design principles, allowing for seamless conversion between them.

The E-R model uses entity sets and relationship sets to define the database structure, while the relational model uses relation schemas, which can be viewed as tables in a database. The conversion of E-R design to relational design requires that for each entity set and relationship set, there is a corresponding relation schema with a unique name.

Constraints are an essential aspect of database design, and the E-R model provides a framework for defining constraints that can be mapped to the relational model. In this regard, this section delves into how E-R schemas can be represented by relation schemas and how constraints from the E-R design can be mapped to constraints on relation schemas.

As such, the conversion of E-R models to relational models enables the use of a more straightforward and flexible approach to database design and management. This technique enhances data integrity, accuracy, and consistency, making it an invaluable tool for modern-day data scientists.

In the world of database management, the conversion of E-R designs into relational designs is a crucial step toward creating efficient and effective database systems. This process involves representing an E-R schema by relation schemas and mapping constraints from the E-R model to those in the relational model.

In this vein, let us explore how strong entity sets with simple descriptive attributes can be represented as relation schemas. If we have a strong entity set E with attributes a1, a2, ..., and an, we can create a schema called E with n distinct attributes to represent it. Here, since student ID is the primary key of the entity set, it is also the primary key of the relation schema.

All the strong entity sets, except the time slot, only have simple attributes. Thus, we can derive the following schemas from these strong entity sets: classroom (building, room number, capacity), department (dept name, building, budget), course (course id, title, credits), instructor (ID, name, salary), and student (ID, name, tot cred). Note that the instructor and student schemas differ from those used in previous chapters as they do not contain the attribute dept name. However, we will revisit this issue shortly.

The handling of strong entity sets with nonsimple attributes can be a challenge. We create separate attributes for each component attribute of a composite attribute, rather than creating a separate attribute for the composite attribute itself. For example, the schema generated for the instructor entity set includes separate attributes for first name, middle name, and last name, rather than creating a separate attribute for the name.

Though not explicitly represented in the relational data model, they can be represented as "methods" in other data models such as the object-relational data model. And for multivalued attributes, we create relation schemas with an attribute corresponding to the primary key of the entity set or relationship set of which the multivalued attribute is a part.

In practice, this means that we create a relational schema for the multivalued attribute phone number of the instructor entity set, with the primary key of the instructor as the corresponding attribute. Each phone number of an instructor is then represented as a unique tuple in relation to this schema. And we create a foreign-key constraint on the relation schema generated from the multivalued attribute, with the attribute generated from the primary key of the entity set referencing the relation generated from the entity set.

We can drop the relation schema for the entity set and retain only the relation schema with the attribute corresponding to the primary-key attribute and the multivalued attribute. For example, the time slot entity set can be represented by a single schema created from the multivalued composite attribute, with time slot id as the primary key.

Drawing upon an encyclopedic knowledge of database design, the author skillfully articulates the mechanics of representing weak entity sets by way of a relation schema, complete with a foreign-key constraint that ensures the existence of a corresponding tuple representing the associated strong entity. The author then takes us through an illustration of this process by way of the weak entity set section in the E-R diagram of Figure 7.15, painting a vivid picture of how the primary key of the course entity set and the discriminator of the section combine to form the primary key of the schema, while also creating a foreign-key constraint on the section schema.

Moving on to the representation of relationship sets, the author masterfully explains the mechanics of choosing a primary key for binary relationship sets, deftly navigating the complexities of one-to-one, many-to-one, and one-to-many relationship sets to arrive at a lucid and insightful conclusion. Through a series of carefully crafted examples, the author walks us through the intricacies of creating foreign-key constraints on relation schema R, deftly leveraging the primary keys of entity sets to create a coherent and well-organized system.

Redundancy can be a hindrance rather than a help. In particular, relationships between weak and strong entity sets can lead to the superfluous schema, as the relationship sets themselves contain no descriptive attributes. This is further complicated by the fact that the primary key of a weak entity set includes the primary key of the strong entity set.

A striking example of this phenomenon can be seen in the E-R diagram, where the weak entity set section is dependent on the strong entity set course through the relationship set sec course. The sec course schema, which includes attributes such as course id, sec id, semester, and year, is redundant when compared to the section schema, which contains the same attributes among others. In fact, every combination of (course id, sec id, semester, year) in a sec course relation can also be found in the section schema, and vice versa. As such, the relationship set schema between weak and strong entity sets is generally unnecessary.

However, in cases where a many-to-one relationship set exists between entity sets A and B, and the participation of A in the relationship is total, we can combine the A and AB schemas to form a single schema.

For example, the schemas instructor and department correspond to the entity sets A and B, respectively, and can be combined to form the inst dept schema. Similarly, the schemas student and department can be combined to form the stud dept schema, while the schemas course and department can be combined to form the course dept schema.

### Entity-Relationship Design Issues

The notions of entity sets and relationship sets are fraught with imprecision. Indeed, the possibilities for defining a set of entities and the relationships that bind them are manifold. In this section, we delve into the fundamental issues that undergird the construction of an entity-relationship (E-R) database schema, with a more detailed exploration of the design process.

One salient question that arises is whether to utilize entity sets or attributes. Take, for instance, the instructor entity set, which could be augmented with an additional attribute - a phone number. However, it is entirely plausible to argue that a phone number should be treated as an entity in its own right, with its own corresponding attributes such as location (e.g. office, home) and type (e.g. mobile, IP phone). In this scenario, the attribute of a phone number would not be added to the instructor entity set, but rather a new entity set of phones would be created, along with a relationship set between instructors and phones, aptly named "inst phone," as seen in Figure below:

![Figure 91 -  Alternatives for adding phone to the instructor entity set](91.png)

But what exactly differentiates these two definitions of an instructor? Well, treating a phone number as an attribute implies that instructors have precisely one phone number apiece. In contrast, treating phones as an entity allows instructors to have multiple phone numbers (even zero) associated with them. That being said, phone numbers could be defined as a multivalued attribute, enabling multiple phones per instructor. So what makes treating a phone as an entity preferable? The answer lies in the extra information one might want to preserve about a phone, such as its location, type, or all individuals who share the same phone. It follows, then, that treating the phone as an entity better models this scenario and is thus more general than treating it as an attribute.

Of course, one might ask what exactly constitutes an attribute versus an entity set. Alas, the answer is not so clear-cut. The distinctions between the two hinge on the structure of the real-world enterprise being modeled and on the semantics associated with the attribute at hand.

A common mistake that people make in E-R database schema design is to utilize the primary key of an entity set as an attribute of another entity set, instead of using a relationship. For instance, it would be incorrect to model the ID of a student as an attribute of an instructor, even if each instructor advises only one student.

The use of entity sets versus relationship sets can be a tricky issue. The question of whether to represent an object as an entity set or a relationship set is not always clear-cut and requires careful consideration. As depicted in Figure, the takes relationship set can be used to model the situation where a student takes a course. However, an alternative approach would be to create a course-registration record for each course that each student takes, and represent it as an entity set called "registration". This entity set would be related to exactly one student and one section, creating two relationship sets: one to relate course-registration records to students, and another to relate them to sections. While both approaches accurately represent the university's information, using the takes relationship set is more concise and efficient.

![Figure 92 -  Replacement of takes by registration and two relationship sets](92.png)

One way to determine whether to use an entity set or a relationship set is to use a relationship set to describe an action that occurs between entities. This approach can also be helpful in deciding which attributes may be more appropriately expressed as relationships.

In addition, it is important to consider whether to use binary or n-ary relationship sets. While relationships in databases are often binary, some relationships that appear to be nonbinary could actually be better represented by several binary relationships. For example, instead of creating a ternary relationship called a parent to relate a child to his/her mother and father, two binary relationships called mother and father could be created. Using binary relationship sets is preferable in this case, as it provides a record of a child's mother even if the father's identity is unknown.

![Figure 93 - Ternary relationship versus three binary relationships](93.png)

It is always possible to replace a nonbinary (n-ary, for n > 2) relationship set by a number of distinct binary relationship sets. This can be done by creating an entity set to represent the relationship set, and then creating three relationship sets to replace the original ternary relationship set. However, this process can increase the complexity of the design and overall storage requirements.

![Figure 94 - Ternary relationship versus three binary relationships](94.png)

In some cases, an n-ary relationship set may be necessary to show that several entities participate in a single relationship. Moreover, there may not be a way to translate constraints on a ternary relationship into constraints on binary relationships. For example, consider the relationship set proj guide, which relates instructors, students, and projects. While it cannot be directly split into binary relationships between instructors and projects, and between instructors and students, doing so may not be very natural.

The placement of relationship attributes can be a perplexing challenge. A cardinality ratio of a relationship can have a profound impact on where to place these attributes. In some cases, attributes of one-to-one or one-to-many relationship sets can be associated with one of the participating entity sets, instead of the relationship set itself.

For instance, let's take the case of an advisor-student relationship, where one instructor may advise several students, but each student can only be advised by a single instructor. In this scenario, the attribute 'date', which specifies the date on which an instructor became the advisor of a student, can be associated with the student entity set, rather than with the advisor relationship set. This is because each student entity participates in a relationship with at most one instance of an instructor. However, this design decision should reflect the characteristics of the enterprise being modeled.

In contrast, the choice of attribute placement is more straightforward for many-to-many relationship sets. In such cases, the attribute must be associated with the many-to-many relationship set itself, rather than with any of the participating entities. This is because the attribute is determined by the combination of the participating entity sets, rather than by either entity separately.

Therefore, the placement of relationship attributes in a database design must be thoughtfully considered to accurately represent the characteristics of the enterprise being modeled.

### Extended E-R Features

The basic E-R model has been the bedrock of database design for decades, but as with any paradigm, there are some aspects that can be better expressed with extensions. In this section, we will explore some of the extended E-R features that can help us model complex databases more effectively.

One such feature is specialization, which allows us to create more specific entity sets from a general entity set. For example, we can create a "student" entity set that specializes from the "person" entity set, with additional attributes such as "major" and "class standing."

Another extension is a generalization, which allows us to group similar entity sets into a more general entity set. For example, we can group the "student" and "instructor" entity sets into a more general "personnel" entity set.

Higher- and lower-level entity sets allow us to organize entity sets into hierarchies. Attribute inheritance is a related feature that allows attributes to be inherited by lower-level entity sets from higher-level entity sets.

Finally, aggregation is an extension that allows us to treat a collection of entities as a single entity. For example, we can treat a department and all of its associated courses as a single entity.

To illustrate these extended E-R features, we will use a more elaborate database schema for a university, which includes an entity set called "person" with attributes such as ID, name, and address. With these tools at our disposal, we can model even the most complex databases with clarity and precision.

In the realm of database modeling, entities within an entity set may have distinct attributes that set them apart from other entities in the same set. Enter the concept of specialization, an extended feature of the E-R model that allows for subgroupings of entities within a set. For example, the entity set "person" may be further classified as an employee or a student, each with their own set of attributes beyond those of the parent entity set.

The university setting provides ample opportunity for specialization. Students can be further categorized as graduate or undergraduate, each with their own unique attributes. Graduate students may have an office assigned to them, while undergraduate students are assigned to a residential college. Similarly, employees can be classified as instructors or secretaries, with their own set of specialized attributes and relationships to other entity sets.

An entity set can be specialized by more than one distinguishing feature, resulting in overlapping specializations, or by at most one feature, resulting in disjoint specializations. This concept is visually represented in an E-R diagram by a hollow arrowhead pointing from the specialized entity set to the other entity set. This relationship is called the ISA relationship and is akin to stating that an instructor "is an" employee.

![Figure 95 - Specialization and generalization](95.png)

It opens the door to subclass relationships, which are crucial to accurately modeling complex data structures.

The refinement of an initial entity set into successive levels of entity subgroupings represents a crucial top-down process in which important distinctions are made explicit. However, the design process may also proceed in a bottom-up fashion, whereby multiple entity sets are synthesized into a higher-level entity set on the basis of common features.

Upon closer inspection, the designer may recognize that the instructor and secretary entity sets share some key attributes, such as their identifier, name, and salary attributes. This commonality can be expressed through generalization, which is a containment relationship that exists between a higher-level entity set and one or more lower-level entity sets.

To illustrate this concept, let's consider the example of an employee entity set that contains both instructors and secretaries as lower-level entity sets. In order to create a generalization, the attributes that are conceptually the same must be given a common name and represented by the higher-level entity of a person. In this way, the attribute names ID, name, and address can be used to create a cohesive and unified schema that accurately reflects the needs of the user.

It's worth noting that higher- and lower-level entity sets can also be referred to as superclass and subclass, respectively. For all practical purposes, generalization is simply the inverse of specialization, and both processes are typically employed in combination during the course of designing an E-R schema for an enterprise. In terms of the E-R diagram itself, there is no need to distinguish between specialization and generalization; rather, new levels of entity representation are distinguished or synthesized as needed to fully express the database application and the user requirements.

While the two approaches may differ in terms of their starting point and overall goal, they ultimately serve the same purpose of creating a robust and effective database schema. The specialization emphasizes differences among entities within a set by creating distinct lower-level entity sets, while generalization synthesizes entity sets into a single, higher-level entity set based on shared attributes and relationship sets. Through the careful application of these techniques, designers can create databases that are efficient, effective, and optimized for the needs of their users.

This crucial property of higher- and lower-level entities created by specialization and generalization brings a level of coherence and structure to an otherwise complex and multifaceted model.

Consider, for instance, the student and employee entities, which inherit the attributes of a person, and are therefore described by their ID name, and address, as well as additional attributes such as tot cred and salary, respectively. And this inheritance, as we learn, applies through all tiers of lower-level entity sets, thus reinforcing the coherence of the model.

But inheritance is not limited to attributes alone; lower-level entity sets also inherit participation in the relationship sets in which their higher-level entities participate. Take, for example, the person entity set that participates in a relationship with the department. This relationship is implicitly inherited by the student, employee, instructor, and secretary entity sets, which also participate in the person dept relationship with the department.

As we explore the implications of ER modeling, it becomes clear that whether the model is arrived at through specialization or generalization, the outcome is largely the same: a higher-level entity set with attributes and relationships that apply to all lower-level entities, and lower-level entity sets with distinctive features that apply only within their own particular sets.

Constraints, however, can be placed on a particular generalization to model an enterprise more accurately. These constraints can involve determining which entities can be members of a lower-level entity set, as in condition-deﬁned or user-defined sets, or whether entities may belong to more than one lower-level set, as in disjoint or overlapping sets. The completeness constraint on a generalization or specialization can also be specified, indicating whether an entity in the higher-level set must belong to at least one of the lower-level sets.

* The Entity-Relationship (E-R) model has proven to be a valuable tool. However, as with any model, it has its limitations. One such limitation is its inability to express relationships among relationships, as illustrated by the ternary relationship proj guide between an instructor, student, and project.
* To capture the evaluation reports required for this relationship, an entity called evaluation is created with a primary key evaluation id. To link evaluations to the (student, project, instructor) combination, a quaternary relationship set eval for between instructor, student, project, and evaluation is created. However, combining the relationship sets proj guide and eval for into a single relationship is not advisable, as some combinations may not have an associated evaluation.

* To avoid redundancy, the concept of aggregation is introduced. Aggregation is an abstraction that treats relationships as higher-level entities. In this case, the relationship set proj guide is treated as a higher-level entity set called proj guide, with a binary relationship eval between proj guide and evaluation representing which (student, project, instructor) combination an evaluation is for.

![Figure 96 - E-R diagram with redundant relationships](96.png)

* The extended E-R features can then be translated into relation schemas. Two methods of designing relation schemas for an E-R diagram that includes generalization are discussed, with foreign-key constraints being a potential issue in the second method.

![Figure 97 - E-R diagram with aggregation](97.png)

In conclusion, the E-R model has proven to be a valuable tool in database design, but its limitations must be considered when dealing with complex relationships. The concept of aggregation offers a powerful solution to overcome these limitations and capture complex relationships with ease.

The representation of aggregation can often pose a challenge. With the aid of the Figure - *E-R diagram with aggregation*, we can easily craft a schema for the relationship set eval that lies between the aggregation of proj guide and the entity set evaluation.

To achieve this, we include an attribute for each attribute in the primary keys of the entity set evaluation and the relationship set proj guide, as well as any descriptive attributes that may exist for the relationship set eval. We then proceed to transform the relationship sets and entity sets within the aggregated entity set according to the well-established rules we have already defined.

The primary key of the aggregation is the primary key of its defining relationship set, and there is no need for a separate relation to representing the aggregation. Instead, the relationships created from the defining relationship are utilized. With these fundamental principles in mind, navigating the complexities of database design can be a far less daunting task.

### Alternative Notations for Modeling Data

In the quest for the most intuitive and effective notation for modeling data, a number of alternatives have been proposed, each with its own unique set of symbols and conventions. Among the most widely used are the Entity-Relationship (E-R) diagram and the Unified Modeling Language (UML) class diagram. These notations play a crucial role in the database schema design process, providing an intuitive and easy-to-understand visual representation of the data model of an application.

![Figure 98 - Symbols used in the E-R notation](98.png)

To provide a basis for comparison, we examine some of the alternative E-R diagram notations as well as the UML class diagram notation. The set of symbols used in our E-R diagram notation is summarized in the Figure above.

Alternative E-R diagram notations include different ways of representing entity and relationship attributes, as well as cardinality constraints and generalization. Some use ovals to represent attributes, with primary key attributes underlined, while others represent relationship attributes by connecting ovals to the diamond representing the relationship. Cardinality constraints can be depicted using various symbols, such as the "crow's-foot" notation, or labels such as "*" and "1."

![Figure 99 - Alternative E-R notations](99.png)

Our new notation, which is closer to the UML class diagram notation, provides a more compact representation of attributes and is supported by many E-R modeling tools. However, it is important to note that different tools may offer various notational variants.

While E-R diagrams are crucial for modeling data representation in a software system, they are only one component of an overall system design. UML provides a standard for creating specifications of various components of a software system, including models of user interactions, functional modules, and their interactions. As such, UML plays a vital role in the design and development of complex software systems.

![Figure 100 - Symbols used in the UML class diagram notation](100.png)

### Other Aspects of Database Design

In exploring the complexities of database design, we must not fall prey to the misguided notion that schema design is the be-all and end-all. There are, in fact, a multitude of factors that must be taken into account when considering the optimal design for a database. We shall only briefly survey a few of these factors here but will delve more deeply into them in future chapters.

One crucial aspect of database design is the implementation of data constraints, which can be expressed using SQL. Constraints serve to ensure consistency in data preservation and can be centrally located and updated, making them more reliable than relying on individual application programs to enforce constraints. Furthermore, the explicit expression of constraints allows for the use of unique identifiers in designing relational database schemas, such as social security numbers, which can be used to link data related to a particular individual across multiple relations.

Performance is another critical consideration in database design, as it affects the efficiency of users and processes interacting with the system. Throughput, which measures the number of queries or updates processed per unit of time, and response time, which measures the time a single transaction takes from start to finish, are the primary metrics for performance. While throughput is the focus of systems processing large numbers of transactions, response time is critical for systems interacting with people or time-critical systems. The type of queries that are expected to be most frequent, as well as the relative mix of update and read operations, are important factors in the choice of indices to speed query evaluation.

Authorization requirements are also a crucial consideration in database design. SQL allows access to be granted to users on the basis of components of the logical design of the database, so relation schemas may need to be decomposed to facilitate access rights. Division of data becomes even more critical when the data are distributed across systems in a computer network, as we shall see in Chapter 19.

In short, there are myriad factors to consider when designing a database beyond schema design, and a holistic approach is necessary to ensure optimal performance and functionality.

## Relational Database Design

In this chapter, the intricate art of relational database design is brought to the fore. Akin to the E-R model, this pursuit aims to create a schema that obviates redundancy while facilitating easy access to stored data. The key to achieving this objective is the crafting of schemas that conform to the appropriate normal form. To accomplish this, an understanding of the enterprise being modeled is vital, and this can be gleaned from a well-crafted E-R diagram or other relevant sources of information.

With this in mind, the chapter introduces a formal method of relational database design predicated on the notion of functional dependencies. Using this method, the team defines normal forms in terms of functional dependencies and other forms of data dependencies. Before delving into the intricacies of this design approach, the chapter scrutinizes the relational design conundrum, focusing on the schemas derived from an extant entity-relationship design. In sum, this chapter offers a masterclass in the design of relational databases.

### Features of Good Relational Designs

In exploring the intricacies of relational database design, we must tread carefully and consider the subtle nuances of our design choices. The allure of creating larger schemas to reduce the complexity of our queries may seem tempting, but we must be wary of the consequences that come with storing redundant information. As we learned from the university database example, the inst dept schema presents a double-edged sword that risks creating inconsistency and hindering the creation of new departments.

![Figure 101 - Schema for the university database](101.png)

Similarly, the decision to split a schema into smaller, more specialized schemas requires a nuanced approach that takes into account the unique rules and functional dependencies of the database.

![Figure 102 - The inst dept table](102.png)

We cannot simply rely on ad-hoc methods of identifying repetition in the data as it may be a mere coincidence or a special case that does not generalize to other scenarios. Instead, we must turn to the fundamental rules and constraints that govern the database and use functional dependencies to guide our schema decomposition.

![Figure 103 - Loss of information via a bad decomposition](103.png)

In short, the art of relational database design requires a delicate balance between simplicity, efficiency, and accuracy. We must constantly weigh the trade-offs between larger and smaller schemas, redundant and non-redundant information, and specialized and generalized functionality. Only through a thoughtful and meticulous approach can we hope to create databases that are both reliable and effective.

### Atomic Domains and First Normal Form

The concept of atomic domains and the first normal form is a fundamental and essential principle. When designing tables from entity-relationship models, which allow for attributes with substructure such as multivalued or composite attributes, we must eliminate this substructure in the relational model. This is achieved by creating a separate attribute for each component of a composite attribute and by creating one tuple for each item in a multivalued set.

In the relational model, we formalize the idea that attributes have no substructure and define an atomic domain as one where the elements are considered indivisible units. A relation schema is in first normal form (1NF) if all attributes have atomic domains. For instance, sets of names or identification numbers with department codes and unique employee numbers are examples of non-atomic domains that would violate 1NF.

Using set-valued attributes can lead to redundant storage and inconsistencies, which can cause problems when updating data. While some types of non-atomic values, such as composite-valued attributes, can be useful, they should be used with care. Forcing a first normal form representation in domains with complex entity structures can create unnecessary burdens on application programmers, who must write code to convert data into an atomic form, and runtime overhead. Nonetheless, modern database systems support various types of non-atomic values.

While some non-atomic values may have utility in certain circumstances, the potential for inconsistencies and redundancy requires careful consideration when using them in database design.

### Decomposition Using Functional Dependencies

In the realm of relational database design, the evaluation of whether a given schema should be decomposed can be achieved via a formal methodology that is grounded in the concepts of keys and functional dependencies. In order to discuss algorithms for database design, it is necessary to use notation that pertains to arbitrary relations and their schema, rather than focusing only on examples. This notation is reminiscent of that introduced in the relational model.

![Figure 104 - Sample instance of relation r](104.png)

In the context of this notation, certain sets of attributes can be used to uniquely identify tuples in a given relation, and these sets are known as superkeys. Keys, candidate keys, and primary keys can be seen as types of real-world constraints that are commonly represented formally. Functional dependencies, on the other hand, allow for constraints that identify the values of certain attributes within a schema.

A functional dependency is said to hold on to a given schema if it is satisfied in every legal instance of that schema. If a set of attributes is a superkey for a relation schema, then the functional dependency between that set and the entire set of attributes of that schema holds. This means that for every pair of tuples in any legal instance of the relation that shares the same superkey, their entire attribute sets will be identical.

Functional dependencies enable the expression of constraints that cannot be represented with superhero. The relationship between superkeys and functional dependencies is demonstrated with the example of a schema involving departments and instructors, in which the functional dependency between the department name and the budget holds, indicating that the department name can be used to uniquely identify the budget of a given department. Ultimately, the concepts of keys and functional dependencies are crucial in the evaluation of whether a given relational schema should be decomposed.

![Figure 105 - An instance of the classroom relation](105.png)

As we delve deeper into the world of database design, we come across the Boyce-Codd normal form (BCNF), a highly desirable state that eliminates all redundancy based on functional dependencies. While there may still be other forms of redundancy remaining, BCNF eradicates any redundancy that can be discovered through functional dependencies. For a relation schema R to be considered in BCNF with respect to a set F of functional dependencies, there must be at least one of the following criteria:

* A functional dependency is trivial, meaning that the dependent attribute is a subset of the determinant.
* The determinant is a superkey for schema R.
* To demonstrate this concept, we revisit the relational schema inst_dept (ID, name, salary, dept_name, building, budget), which we previously saw was not in BCNF due to the functional dependency dept_name → budget. As dept_name is not a superkey, we decompose inst_dept into instructor and department. Upon doing so, we discover that the instructor is in BCNF, with ID being the primary key and a superkey for the schema. Similarly, the department is also in BCNF, with dept_name being the primary key and a superkey for the schema.
* When a schema is not in BCNF, we must decompose it to remove the redundancy. To do so, we replace R in our design with two schemas, (Lambda U Beta) and(R - (Beta - Lambda). In the case of inst_dept, we replace it with (dept_name, building, budget) and (ID, name, dept_name, salary). This process continues until all resulting schemas are in BCNF.

![Figure 106 - The dept advisor relationship set](106.png)

While BCNF is highly desirable, it may hinder the efficient testing of certain functional dependencies if the decomposition is not done properly. This is because testing constraints each time the database is updated can be costly. Therefore, designing the database in a way that allows for efficient constraint testing is crucial.

### Functional-Dependency Theory

In a world driven by data, the ability to reason systematically about functional dependencies is a fundamental skill for anyone working with databases. Functional-Dependency Theory, as exemplified in the groundbreaking work of Armstrong, provides a powerful framework for reasoning about these dependencies and ensuring that database schemas conform to desired normal forms.

The crux of the theory lies in the concept of logical implication: given a set of functional dependencies F on a schema, we can prove that certain other functional dependencies hold on the schema. In other words, we can determine which dependencies are "logically implied" by F. However, this process can be time-consuming, particularly for large sets of dependencies.

![Figure 107 -  A procedure to compute F+](107.png)

To address this issue, Armstrong's axioms provide a set of rules for inferring additional dependencies from a given set. These axioms are both sound and complete, meaning they generate all correct dependencies and no incorrect ones. Moreover, they can be used to prove the correctness of additional rules, such as the Union rule, Decomposition rule, and Pseudotransitivity rule.

![Figure 108 -  An algorithm to compute a+](108.png)

In practice, the ability to reason about functional dependencies is critical for ensuring the accuracy and efficiency of databases. Whether working with small or large sets of dependencies, understanding the principles of Functional-Dependency Theory and Armstrong's axioms is essential for anyone seeking to master this field.

Ensuring the satisfaction of functional dependencies (FDs) in a given relation schema is paramount. Such satisfaction guarantees the integrity and consistency of the data and is a fundamental requirement of any reliable database system. By checking the satisfaction of FDs on every update can be computationally expensive, especially for large datasets.

The canonical cover is a simplified set of FDs that has the same closure as the original set. It is obtained by eliminating extraneous attributes from each FD in the set until no extraneous attributes remain. An extraneous attribute is one that can be removed from a given FD without altering its closure. In other words, it is a redundant attribute that does not contribute to the satisfaction of the FD.

The process of computing the canonical cover involves iteratively removing extraneous attributes from each FD in the set until a fixed point is reached. This can be done efficiently by computing the closures of the set of FDs with and without each extraneous attribute. If the closure of the FD set with the extraneous attribute is the same as the closure of the FD set without the attribute, then the attribute is extraneous and can be safely removed.

Once we have obtained the canonical cover of a set of FDs, we can use it to check the satisfaction of FDs on updates. This is because any relation that satisfies the canonical cover also satisfies the original set of FDs and vice versa. Furthermore, the canonical cover has unique left sides and no extraneous attributes, making it an ideal representation of the minimal set of FDs required for the satisfaction of the original set.

A canonical cover is a powerful tool for reducing the complexity of FD satisfaction checks in relational databases. It allows us to obtain a simplified set of FDs that is equivalent to the original set while removing any redundancy and ensuring minimalism. With the canonical cover, we can ensure the integrity and consistency of our data, without sacrificing performance or scalability.

### Algorithms for Decomposition

In the world of database design, lossless decomposition is a concept of utmost importance. This principle states that a database schema, defined by a relation schema r(R) and a set of functional dependencies F, can be decomposed into two relation schemas, r1(R1) and r2(R2), without losing any information, as long as the original relation r contains the same set of tuples as the result of a natural join of the projection of r onto R1 and R2. This lossless join decomposition is crucial in ensuring that the database remains consistent and complete even after the decomposition process.

However, not all decompositions are lossless. A lossy decomposition occurs when information is lost during the decomposition process, resulting in a joint result that is a superset of the original relation but lacks certain key information. To avoid this, it is essential to test whether decomposition is lossless or not. This can be done using functional dependencies, where a decomposition is lossless if R1 ∩ R2 forms a superkey of either R1 or R2.

Another important concept in database design is dependency preservation. This principle states that a decomposition of a schema R into multiple schemas should preserve all the functional dependencies of the original schema. To test this, we can restrict the set of functional dependencies to each individual relation schema, and verify that the union of these restrictions implies all the original functional dependencies. If this is the case, then the decomposition is said to be dependency-preserving.

![Figure 109 -  Testing for dependency preservation](109.png)

While these concepts may seem complex and technical, they are essential in ensuring that databases remain consistent and complete, and that data is not lost during the decomposition process. By understanding lossless decomposition and dependency preservation, we can design databases that are robust, efficient, and accurate.

As we delve into the intricacies of database design, we are faced with the challenge of developing designs that adhere to the rules of appropriate normal form. It is for this reason that we require algorithms to assist in the generation of such designs, and in this section, we shall explore algorithms for BCNF and 3NF.

To begin with, we must test whether a relation schema is in BCNF, and while the definition of BCNF can be used for this purpose, the computation of F + can prove to be a tedious task. However, simplified tests can be performed to verify whether a nontrivial dependency causes a violation of BCNF. Additionally, it is important to note that the testing procedure cannot be employed when a relation is decomposed, as it may not be sufficient to use F to test a decomposed relation for a BCNF violation. Therefore, we may require a dependency that is in F+, but not in F, to demonstrate that a decomposed relation is not in BCNF.

![Figure 110 -  BCNF decomposition algorithm](110.png)

An alternative BCNF test can be applied to check if a relation in a decomposition of R satisfies BCNF. The algorithm uses dependencies that demonstrate the violation of BCNF to perform the decomposition, generating not only BCNF schemas but also a lossless decomposition. However, it is important to note that the BCNF decomposition algorithm takes exponential time, and while there are algorithms that can compute a BCNF decomposition in polynomial time, they may "over-normalize" by decomposing a relation unnecessarily.

![Figure 111 -  Dependency-preserving, lossless decomposition into 3NF](111.png)

As an example of the practical application of the BCNF decomposition algorithm, let us consider a database design using the class schema. We must ensure that the set of functional dependencies that we require to hold on class are satisfied, and we can employ the BCNF decomposition algorithm to achieve this end. Ultimately, we must remember that the development of a robust database design requires a thorough understanding of the underlying principles and a careful application of algorithms and testing procedures to ensure adherence to the rules of appropriate normal form.

In the realm of relational database schemas, the 3NF algorithm stands as a stalwart, a beacon of hope in a sea of uncertainty. Building a schema for each dependency in a canonical cover preserves dependencies and ensures a lossless decomposition. Though not uniquely defined and subject to the order in which dependencies are considered, the algorithm guarantees 3NF even for relations already in the form.

BCNF and 3NF both offer advantages, but the latter allows for the preservation of dependencies without sacrificing losslessness. However, it comes with the caveat of potential repetition of information and null values to represent relationships. When designing databases with functional dependencies, our goals are to achieve BCNF, losslessness, and dependency preservation, but it's not always possible to satisfy all three. In such cases, we must choose between BCNF and dependency preservation with 3NF.

It's worth noting that SQL lacks a way to specify functional dependencies, except for the declaration of superkeys with primary or unique constraints. While assertions can enforce functional dependencies, no database system currently supports such complex assertions. Even with a dependency-preserving decomposition, standard SQL can only efficiently test dependencies with a left-hand side that is key. However, materialized views can reduce the cost of testing functional dependencies, provided the database system supports primary key constraints on materialized views.

### Decomposition Using Multivalued Dependencies

In the realm of database normalization, even the most sophisticated normalization technique, such as Boyce-Codd normal form (BCNF), can sometimes fail to eliminate the problem of redundant information in certain relation schemas. Take for instance the scenario where a university instructor is associated with multiple departments. Although BCNF can be applied to this schema, it still suffers from redundant information due to the repetition of an instructor's address information for each department they are affiliated with.

To address this issue, a new form of constraint, called multivalued dependencies (MVDs), must be introduced. While functional dependencies determine the presence or absence of certain tuples in a relation, MVDs require certain other tuples to be present. Multivalued dependencies are thus referred to as tuple-generating dependencies.

In a relation schema r(R), a multivalued dependency A →→ B holds if, in any legal instance of relation r(R), for all pairs of tuples t1 and t2 in r such that t1[A] = t2[A], there exist tuples t3 and t4 in r that satisfy certain conditions. If the multivalued dependency A →→ B is satisfied by all relations on schema R, it is considered a trivial multivalued dependency on schema R.

![Figure 112 -  Tabular representation](112.png)

To better illustrate the distinction between functional and multivalued dependencies, consider the scenario of a university instructor with multiple addresses and affiliations with multiple departments. By applying the multivalued dependency ID →→ street, city, we can eliminate the redundancy of repeating an instructor's address information for each department they are associated with.

![Figure 113 -  An example of redundancy in a relation on a BCNF schema](113.png)

![Figure 114 -  An illegal r2 relation](114.png)

While BCNF is a powerful tool for normalization, it may not always suffice in eliminating redundancy in relation schemas. Multivalued dependencies offer an effective means of addressing this issue by specifying conditions that must be met to ensure the presence of certain tuples in a relation.

Specifically, we explore the intricacies of the Fourth Normal Form (4NF), which is a level of schema normalization that addresses the issue of multivalued dependencies.

To determine if each relation schema in a decomposition satisfies 4NF, we must first identify the multivalued dependencies that exist within each schema. To do so, we define the restriction Fi of a set of functional dependencies F to Ri, which includes all functional dependencies in F+ that involve only attributes of Ri. We also consider a set D of both functional and multivalued dependencies, and the restriction of D to Ri, which is the set Di consisting of functional dependencies and multivalued dependencies that only involve attributes of Ri.

The algorithm for decomposing a schema into 4NF closely mirrors that of BCNF, but incorporates multivalued dependencies and uses the restriction of D+ to Ri. If we apply this algorithm to a schema such as (ID, dept name, street, city), we may discover nontrivial multivalued dependencies such as ID→→dept name, indicating the need for further decomposition. By replacing the problematic attribute with two schemas that satisfy 4NF, we can eliminate redundancy and improve schema design.

To ensure that our decompositions are lossless and preserve dependencies, we turn to the concept of multivalued dependencies and their relationship to losslessness. Specifically, we must verify that at least one of two multivalued dependencies holds true for a given decomposition to be considered lossless. The issue of preserving dependencies in the presence of multivalued dependencies is a complex one and requires further exploration.

### More Normal Forms

The fourth normal form (4NF) is a powerful tool in database normalization, but it is not the end-all-be-all of normal forms. In fact, there are several more normal forms that can help us eliminate data redundancy and ensure data integrity. Join dependencies can lead to a higher level of normalization, known as the project-join normal form (PJNF), which is sometimes referred to as the fifth normal form.

But PJNF is not the final frontier of normalization. There is a class of even more general constraints that lead to another normal form called domain-key normal form (DKNF). However, while these generalized constraints can help eliminate data redundancy, they are often difficult to reason about and there is no set of sound and complete inference rules to reason about them. As a result, PJNF and DKNF are rarely used in practice.

Interestingly, the second normal form (2NF) is not discussed at length in this discussion of normal forms. While it has historical significance, its utility has been overshadowed by the more powerful and widely used third normal form (3NF) and beyond. However, it is still a valuable tool to experiment with and gain a deeper understanding of database normalization.

### Database-Design Process

In delving deeper into the intricate details of the database-design process, we have uncovered significant insights that shed light on the complex interplay between the normalization of relation schemas and the broader context of database design. Our exploration has revealed that there are several paths by which a relation schema can be derived, including generating a schema from an E-R diagram, starting with a single relation schema and breaking it down through normalization, or designing relations ad-hoc and verifying their conformance to a desired normal form.

One key issue that emerges when generating relation schemas from E-R diagrams is the potential for functional dependencies between entity attributes to arise. For example, an instructor entity set may have attributes such as department name and department address, with a functional dependency between the former and the latter. In such cases, the normalization process becomes necessary to ensure that the generated relation schema meets the desired normal form. This underscores the importance of designing E-R diagrams with the utmost care, to avoid such issues and ensure that the normalization process can be carried out with minimal adjustments.

Moreover, we have seen that functional dependencies are useful for detecting poor E-R design and that the normalization process can be carried out formally as part of data modeling or left to the designer's intuition during E-R modeling. The universal-relation approach to relational database design assumes a single schema containing all attributes of interest, which defines how users and applications interact with the database.

In addition, we have explored the importance of unique attribute naming, which ensures that each attribute has a unique meaning in the database, preventing confusion between the same attribute used in different schemas. On the other hand, attributes of different relations that have the same meaning can be named identically to reduce user errors. The order of attribute names in a schema may not matter technically, but primary-key attributes are conventionally listed first to make reading default output easier.

In conclusion, our comprehensive analysis of the database-design process has illuminated the various nuances and subtleties involved, highlighting the importance of careful E-R diagram design, functional dependencies, normalization, and unique attribute naming. These insights will undoubtedly prove invaluable for database designers and developers seeking to optimize the design and functionality of their databases.

### Modeling Temporal Data

In a world where temporal data reigns supreme, modeling such data can prove to be a challenging task. Consider, for instance, an instructor entity set and its associated time-varying addresses. To imbue these addresses with temporal information, one must create a multivalued attribute consisting of composite values containing an address and a time interval. But this is just the beginning of the complexity that arises when dealing with temporal data.

Entities themselves may possess valid time intervals, such as the student entity, which has a valid time from the date of entry to the date of graduation or leaving the university. Relationships too can have valid times, as in the case of the prereq relationship, which records when a course becomes a prerequisite for another course.

Adding such temporal details to an E-R diagram is no mean feat, for it can make the diagram difficult to create and comprehend. While there have been several proposals to extend the E-R notation to account for temporal data, there are no universally accepted standards.

To compound matters further, functional dependencies that we assumed to hold for regular data may no longer hold when tracking data values over time. Instead, we must turn to temporal functional dependencies, which hold on a relation schema if all snapshots of that schema satisfy the functional dependency X→Y. While we could extend the theory of relational database design to account for temporal functional dependencies, few designers are prepared to tackle this level of complexity.

As a result, many database designers opt for simpler approaches, such as designing the database ignoring temporal changes, and then adding valid time information to each relation that requires it. This involves adding start and end time attributes, as in the case of the course relation, which may have multiple records with different titles and corresponding valid time ranges. If the relation is updated, a new tuple is added containing the new title and start time, and the end time of the previous tuple is updated accordingly.

However, when a relation has a foreign key referencing a temporal relation, the database designer must decide whether the reference is to the current version of the data or to the data as of a specific point in time. For example, while a student's transcript should refer to the course title at the time the student took the course, a reference from the instructor or student relation may only care about the current version of the data.

All of these complexities make modeling temporal data a formidable challenge, one that requires careful consideration and attention to detail. But with the right approach and a deep understanding of the underlying principles, it is possible to tame the beast that is temporal data and extract valuable insights that can inform decision-making at every level of the organization.

## Application Design and Development

The ubiquitous use of databases in today's world occurs primarily through application programs. As a result, user interaction with databases is largely indirect, taking place through the medium of these programs. In response to this, database systems have incorporated tools such as form and GUI builders, which streamline the development of applications that interface with users. However, with the emergence of the Web as the primary mode of user interaction, the focus has shifted toward the development of Web-based applications that rely on databases to store data.

In this chapter on application design and development, we explore the various tools and technologies utilized in the creation of interactive applications that employ databases to manage data. After a brief introduction to application programs and user interfaces, we delve into the world of Web-based applications, providing an overview of relevant Web technologies. Into the widely utilized Java Servlets technology for building Web applications, followed by a succinct overview of Web application architectures.

To streamline the process of application development, we examine the tools available for rapid application development, while in the following section, we turn our attention to the crucial issue of performance when building large-scale Web applications. Afterward, we consider the paramount issue of application security, followed by a comprehensive discussion on encryption and its implementation in applications.

In conclusion, this chapter offers a comprehensive exploration of the tools and technologies employed in the development of interactive applications that rely on databases to manage data. It highlights the significance of Web-based applications in today's world and offers insights into key issues such as performance and security, ensuring that the reader is well-equipped to tackle the challenges of building successful applications in this arena.

### Application Programs and User Interfaces

In the realm of database systems, the majority of users are not familiar with the use of query languages to directly interact with the system. Instead, application programs serve as a crucial intermediary, offering a user interface at the front end while communicating with the database at the back end. These applications accept user input through forms-based interfaces, allowing for data entry or information retrieval from the database based on the user's input. This output is then presented to the user.

One example of an application program is a university registration system. This type of system typically requires users to first authenticate themselves with a username and password, after which the system retrieves information about the user from the database, such as registered courses and name and presents it to them. The application offers users the ability to register for courses or query information about courses and instructors. Such applications are used in a variety of industries to automate tasks ranging from sales and accounting to human resources management and inventory management.

Some application programs are used even without the user's awareness, such as when a news site offers users a personalized page based on their browsing history. In this case, an application program generates a customized page for each user, taking into account their history of articles viewed. Application programs typically have a front-end component for the user interface, a back-end component for database communication, and a middle layer containing "business logic" that handles specific requests for information or updates.

![Figure 116 - Application architectures in different eras](116.png)

The evolution of application architectures over time is depicted in the Figure, with airline reservations serving as an example of an application that has been around since the 1960s. Early computer applications were run on mainframe computers, with users interacting through terminals that often supported forms. The rise of personal computers brought with it a client-server architecture, which allowed for powerful graphical user interfaces. However, installing software on each user's computer made upgrades more difficult. In recent years, web browsers have become the go-to front end for database applications, using the standardized syntax of HyperText Markup Language (HTML) to create forms-based interfaces.

Unlike client-server architectures, web-based applications do not require any application-specific software to be installed on client machines. JavaScript programs are used to create sophisticated user interfaces and can be run in a safe mode that ensures security. These programs are downloaded to the browser transparently and do not require explicit installation on the user's computer. Application programs are executed on a web server in response to requests from a browser, with a variety of technologies available for creating such programs.

In the following chapter, we delve into the technologies and tools used to build web interfaces and application programs, as well as application architectures, performance, and security concerns.

### Web Fundamentals

As we delve into the world of the World Wide Web, we must first acquaint ourselves with its fundamental technology. For those unfamiliar with the underlying infrastructure, let us begin with a discussion on Uniform Resource Locators (URLs).

A URL is a globally unique name for each document that can be accessed on the Web. It consists of various parts that identify the document's location and how it is to be accessed. For instance, the "http" at the beginning of a URL indicates that the document is to be accessed by the HyperText Transfer Protocol (HTTP), which is a protocol for transferring HTML documents. The second part of the URL gives the name of a machine that has a Web server, while the rest of the URL is the path name of the file on the machine or other unique identifier of a document within the machine.

![Figure 117 - Tabular data in HTML format](117.png)

Furthermore, a URL can contain the identifier of a program located on the Web server machine, as well as arguments to be given to the program. When a request is received for such a URL, the Web server executes the program, using the given arguments, and returns an HTML document to the Web server, which sends it back to the front end.

![Figure 118 - Display of HTML source](118.png)

![Figure 119 - An HTML form](119.png)

Moving on to HyperText Markup Language (HTML) is the language used to create web pages, allowing for the structuring of text, images, and other media on a webpage. HTML pages are enclosed in an HTML tag, while the body of the page is enclosed in a body tag. A table is specified by a table tag, which contains rows specified by a tr tag, and so on. The use of HTML tags allows for the creation of forms, menus, and tables, making it easier for web designers to create visually appealing websites.

![Figure 120 - Display of HTML source](120.png)

But the power of the Web does not stop there, as Web servers provide an array of features beyond the mere transfer of documents. By executing programs with user-supplied arguments, a Web server can act as an intermediary to provide access to a variety of information services. The Common Gateway Interface (CGI) standard defines how the Web server communicates with application programs, allowing for the creation of new services by installing an application program that provides the service.

![Figure 121 - Three-layer Web application architecture](121.png)

[Figure 122 - Two-layer Web application architecture](122.png)

As we marvel at the sheer magnitude of the World Wide Web, we must also acknowledge the intricate technology that makes it all possible. With the use of URLs, HTML, and Web servers, we are able to create and access a seemingly infinite world of information at our fingertips.

### Servlets and JSP

In a two-layer web architecture, Java programs can be loaded into the web server itself to implement an application programming interface for communication between the server and the application program. This is known as the Java servlet specification. The HttpServlet class in Java is responsible for implementing the servlet API specification, and subclasses of this class are used to define specific functions. A servlet is essentially a Java program that implements the servlet interface, with the task of processing HTTP requests, accessing databases, and dynamically generating HTML pages for client browsers.

![Figure 123 - Example of servlet code](123.png)

To generate dynamic responses to HTTP requests, servlets are commonly used to access inputs provided through HTML forms, apply business logic, and generate HTML output to be sent back to the browser. A servlet example, PersonQueryServlet, demonstrates the form in the Figure, with the servlet code responsible for extracting values of the parameter type and number using request.getParameter(), running a query against a database, and returning the results of the query to the requester by outputting them to the HttpServletResponse object response.

![Figure 124 - A JSP page with embedded Java code](124.png)

In dealing with the stateless interaction between a browser and a web server, the servlet API provides a method of tracking sessions and storing session information. Using getSession(false) retrieves the HttpSession object corresponding to the browser that sent the request, allowing the server to ask the client to return a cookie with a specified name. If the client returns a value that does not match any ongoing session, then the request is not part of an ongoing session, with getSession() returning a null value, and the servlet directing the user to a login page.

The servlet life cycle begins with loading the servlet class, initializing the servlet by invoking the init() method once, and then handling the service requests using the service() method. Multiple requests can be handled in parallel, with each request resulting in a new thread within which the call is executed. The destroy() method is then invoked to take the servlet out of service, destroying the servlet instance once it is no longer needed.

Thus, Java servlets and JSPs provide a powerful tool for building web applications, allowing for dynamic processing of HTTP requests, session tracking, and a robust life cycle.

The emergence of client-side scripting has transformed the static, text-and-graphic-based Web pages of yesteryear into dynamic and interactive platforms for communication and commerce. By embedding program code within documents, web developers have opened up a world of possibilities for engaging with users beyond the limited confines of HTML and forms. This allows Web pages to perform activities such as animation and validation checks in real-time, all while executing programs on the client side, thereby speeding up interaction significantly. However, with great power comes great responsibility, and if the design of the system is done carelessly, program code embedded in a Web page can perform malicious actions on the user’s computer.

Java, with its platform-independent "byte-code", became a popular solution for executing programs on users' computers, thanks to its safe mode that restricts programs from performing destructive actions. Similarly, simpler scripting languages, such as JavaScript, have emerged as the go-to solution for enriching user interaction while providing protection similar to Java. JavaScript, in particular, has become ubiquitous in the current generation of Web interfaces, allowing web developers to construct sophisticated user interfaces that perform error checks on user input, dynamically modify HTML code, and communicate asynchronously with the Web server.

![Figure 125 - Example of JavaScript used to validate form input](125.png)

Although the JavaScript language has been standardized, differences between browsers, especially in the details of the Document Object Model (DOM) model, can create problems for developers. To mitigate this, web developers often use JavaScript libraries, such as Yahoo's YUI library, that provide browser-independent functions that are optimized for different platforms.

In conclusion, the emergence of client-side scripting has revolutionized the way we interact with the Web, allowing us to create dynamic and interactive platforms for communication and commerce. While the power of this technology is undeniable, it is crucial to use it responsibly and with care, to avoid malicious attacks and protect users' privacy and security.

### Application Architectures

In the intricate world of software development, the architecture of large applications is often broken down into several layers to manage their complexity. The presentation or user interface layer, responsible for user interaction, is often conceptually divided further into distinct layers, based on the model-view-controller architecture. This approach allows for the creation of different views of an application, depending on the software or device used to access it.

The business-logic layer, which provides a high-level view of data and actions on data, is where entities and actions are abstracted. For example, in an application designed for managing a university, the business-logic layer may provide abstractions for entities such as students, instructors, courses, and sections. In addition, workflows are included in the business logic, describing how a particular task is handled when it involves multiple participants. Error situations are also dealt with in this layer.

The data access layer provides the interface between the business-logic layer and the underlying database. This layer is particularly important when using an object-oriented language to code the business-logic layer, as the data-access layer is responsible for mapping the object-oriented data model used by the business logic to the relational model supported by the database. Object-relational mapping, which automates this mapping process, is used to create in-memory objects on demand, as well as to store updated objects back as relations in the database.

Various systems have been developed to implement object-relational mapping, including Hibernate, which is widely used for mapping from Java objects to relations. A mapping file specifies how each Java class is mapped to one or more relations, with information about the database specified in a properties file. This automated approach to mapping data models not only reduces the potential for errors but also increases efficiency, making the task less cumbersome.

![Figure 126 - Web application architecture](126.png)

The architecture of web applications is critical, as it impacts not only the development process but also the overall performance of the application. By breaking down the application into various layers, such as the presentation layer, the business logic layer, and the data access layer, developers can manage complexity more effectively, ensuring that business rules are satisfied and workflows are followed correctly.

### Rapid Application Development

In the realm of web development, the creation of user interfaces can be a significant challenge, requiring considerable programming effort to construct elements such as menus, forms, and result displays. However, several techniques have emerged to reduce the burden of building these interfaces.

One such approach is the provision of pre-built libraries of functions to generate user-interface elements with minimal programming, thereby allowing developers to focus more on business logic and database access. Additionally, drag-and-drop features in integrated development environments enable developers to drag user-interface elements from a menu into a design view of a page, with the IDE generating code that invokes library functions to create the element.

Furthermore, automatic code generation from a declarative specification can simplify user interface development by reducing the amount of manual coding required. These approaches have been part of Rapid Application Development (RAD) tools for many years and are now widely used for creating web applications as well.

Tools such as Oracle Forms, Sybase PowerBuilder, and Oracle Application Express (APEX) have been designed for the rapid development of interfaces for database applications, while others such as Visual Studio and Netbeans VisualWeb support several features designed for the rapid development of web interfaces for database-backed applications.

To minimize the amount of code required to build user interfaces, many HTML constructs are generated using appropriately defined functions rather than being written as part of the code of each web page. For instance, menus can be generated from data in the database using a function that executes a database query and populates the menu using the query result. Similarly, forms that require validation can be generated using functions that output JavaScript code to perform validation at the browser.

Displaying a set of results from a query is a common task for many database applications, and a generic function can be built to take an SQL query as an argument and display the tuples in the query result in a tabular form. Pagination of results can also be implemented to handle situations where the query result is very large.

![Figure 127 - A formatted report](127.png)

While there is no widely used standard Java API for carrying out user-interface tasks, tools such as JavaServer Faces (JSF) and Microsoft's Active Server Pages (ASP) provide a variety of controls that simplify the construction of web interfaces. These controls, such as drop-down menus and list boxes, can be associated with a DataSet object, which is similar to a JDBC ResultSet object and is typically created by executing a query on the database.

Moreover, validator controls can be added to form input fields to specify validity constraints, and error messages to be displayed on invalid input can be associated with each validator control. Overall, these techniques have revolutionized the development of user interfaces for web applications, greatly reducing the effort required and making web development more accessible to developers of all skill levels.

### Application Performance

Web developers face a Herculean task when it comes to ensuring fast response times for millions of users accessing their websites from all corners of the world. The challenge is compounded by the need to handle thousands of requests per second, if not more, for the most popular sites. To achieve this, developers employ a range of techniques to speed up processing and reduce overhead, such as caching and parallel processing.

One technique that has proved effective in reducing overhead is connection pooling. With connection pooling, the application server creates a pool of open JDBC/ODBC connections and makes them available to the code servicing user requests. This eliminates the need to open a new connection to the database for each request, which can take several milliseconds and quickly become a bottleneck. The connection pool manager ensures that the maximum number of concurrent connections supported by the database is not exceeded, and closes any open connections that have not been used for a while.

Web developers must also be vigilant about closing open connections to avoid overwhelming the database. Failure to do so can lead to the database reaching its limit for concurrent open connections, which only becomes apparent under heavy usage.

Another effective technique for reducing costs is caching query results and web pages. By caching query results, developers can avoid repeated communication with the database for identical queries, greatly reducing overhead. Similarly, caching the final web page sent in response to a request can also eliminate the need to recompute the page when a new request with the same parameters comes in. Caching can be done at the fragment level or for complete web pages.

Parallel processing is another popular technique used to handle heavy loads. This involves using multiple application servers to handle user requests in parallel, with a web server or network router used to route each request to a different application server. All requests from a particular client session must go to the same application server, to maintain the session state. However, the database is shared by all application servers, which can become a bottleneck if not properly managed. To avoid this, developers must minimize the number of requests to the database and employ parallel database systems where necessary.

### Application Security

In today's technology landscape, ensuring application security has become a matter of utmost importance. With the increasing threat of hackers and malicious attacks, organizations must take proactive measures to safeguard their applications from potential vulnerabilities.

Beyond the conventional SQL authorization protocols, application security must tackle several security issues that arise due to poorly written application code. The initial point where security must be enforced is within the application itself. To achieve this, applications must authenticate users and restrict users to only authorized tasks.

Despite the database system's robust security measures, an application's security can still be compromised due to several security loopholes. In this regard, the section first sheds light on the loopholes that hackers can exploit to bypass authentication and authorization checks. Subsequently, the section describes techniques for secure authentication, fine-grained authorization, and audit trails that aid in recovering from unauthorized access and erroneous updates. Finally, the section concludes by highlighting issues concerning data privacy.

Among the most significant security threats that applications face are SQL injection attacks, whereby hackers manipulate an application into executing an SQL query crafted by the attacker. To avoid such attacks, the best practice is to employ prepared statements that automatically add escape characters, making it impossible for user-supplied quotes to terminate strings. Additionally, applications that create queries dynamically must ensure that the input string is one of the allowed values to avoid this kind of SQL injection.

Another significant security concern is the potential for cross-site scripting (XSS) attacks, which allow malicious users to enter client-side scripting languages instead of valid names or comments, potentially executing scripts that send private cookie information back to the attacker or execute an action on a different web server. To prevent such attacks, organizations must ensure that their applications incorporate measures such as proper input validation and output encoding to eliminate potential vulnerabilities.

Proactive measures such as robust application security are critical to safeguarding against malicious attacks. By implementing best practices and following recommended guidelines, organizations can protect their applications from potential vulnerabilities and secure their data and sensitive information against unauthorized access.

In today's technology landscape, ensuring application security has become a matter of utmost importance. With the increasing threat of hackers and malicious attacks, organizations must take proactive measures to safeguard their applications from potential vulnerabilities.

Beyond the conventional SQL authorization protocols, application security must tackle several security issues that arise due to poorly written application code. The initial point where security must be enforced is within the application itself. To achieve this, applications must authenticate users and restrict users to only authorized tasks.

Despite the database system's robust security measures, an application's security can still be compromised due to several security loopholes. In this regard, the section first sheds light on the loopholes that hackers can exploit to bypass authentication and authorization checks. Subsequently, the section describes techniques for secure authentication, fine-grained authorization, and audit trails that aid in recovering from unauthorized access and erroneous updates. Finally, the section concludes by highlighting issues concerning data privacy.

Among the most significant security threats that applications face are SQL injection attacks, whereby hackers manipulate an application into executing an SQL query crafted by the attacker. To avoid such attacks, the best practice is to employ prepared statements that automatically add escape characters, making it impossible for user-supplied quotes to terminate strings. Additionally, applications that create queries dynamically must ensure that the input string is one of the allowed values to avoid this kind of SQL injection.

Another significant security concern is the potential for cross-site scripting (XSS) attacks, which allow malicious users to enter client-side scripting languages instead of valid names or comments, potentially executing scripts that send private cookie information back to the attacker or execute an action on a different web server. To prevent such attacks, organizations must ensure that their applications incorporate measures such as proper input validation and output encoding to eliminate potential vulnerabilities.

In a world where data breaches and cyber-attacks pose significant risks to organizations, proactive measures such as robust application security are critical to safeguarding against malicious attacks. By implementing best practices and following recommended guidelines, organizations can protect their applications from potential vulnerabilities and secure their data and sensitive information against unauthorized access.

### Encryption and Its Applications

In a world that is increasingly reliant on technology, encryption has become a critical component for securing sensitive data. From credit-card numbers to fingerprints and social security numbers, businesses and organizations must safeguard this information from cybercriminals who seek to exploit it for personal gain.

Encryption, the process of transforming data into an unreadable form that can only be reversed through decryption, has a long history dating back to the transmission of messages between senders and recipients who shared a secret key. However, as technology has advanced, encryption has become more sophisticated and is now widely used in a range of applications, such as data transfer on the Internet and cellular phone networks.

But not all encryption techniques are created equal. Simple encryption methods, such as substituting each character with the next letter in the alphabet, may be vulnerable to hacking by unauthorized users. A strong encryption technique, on the other hand, must be relatively simple for authorized users to encrypt and decrypt data, and it must rely on the encryption key - rather than the algorithm itself - to keep data secure.

One of the most widely-used encryption techniques today is the Advanced Encryption Standard (AES), a symmetric-key algorithm that operates on a 128-bit block of data at a time, with encryption keys that can be 128, 192, or 256 bits in length. AES was adopted as an encryption standard by the U.S. government in 2000 and is known for its robustness in safeguarding sensitive data.

Despite the effectiveness of encryption, however, it is only as secure as the mechanism used to transmit the encryption key to authorized users. This vulnerability has prompted the development of alternative encryption schemes, such as public-key encryption, which uses two keys - a public key and a private key - to encrypt and decrypt data. Each user has a public key that is published and a private key that is known only to them, ensuring that unauthorized users are unable to access sensitive data.

Encryption is a critical tool for safeguarding sensitive information. As businesses and organizations continue to store more and more data, the need for effective encryption techniques has never been greater.

Digital signatures and digital certificates play a crucial role in authentication and non-repudiation in the world of cryptography. Public-key encryption is used to create digital signatures that act as electronic signatures for documents. The private key is used to sign the data, which can then be made public. Anyone can verify the signature using the public key, but only the person with the private key could have created the signature. This provides a way to authenticate data and verify that it was created by the person who claims to have created it.

Digital certificates are a two-way authentication process used to ensure that a client is interacting with an authentic website. The public key of the site is signed by a certification agency, whose public key is widely known. The root certification authorities' public keys are stored in standard web browsers. The system uses a multi-level approach to reduce the burden of creating certificates on the root certification authorities. The digital certificate contains the name of the party to whom it was issued, the party's public key, and the public key of the certifying authority.

To verify a certificate, the encrypted text is decrypted using the public key to retrieve the name of the party and authenticate the public key for the site. Digital certificates are widely used in HTTPS to authenticate websites to users and prevent malicious sites from masquerading as other websites. The site provides its digital certificate to the browser, which uses the provided public key to encrypt data. The browser creates a one-time symmetric key after authentication, which reduces encryption costs. Digital certificates can also be used for authenticating users by submitting a digital certificate containing the user's public key to a site. The certificate is verified by a trusted authority, and the user's public key can be used to authenticate the user using a challenge-response system.

Digital signatures and digital certificates are crucial for authentication and non-repudiation in the world of cryptography. These techniques use public-key encryption and a multi-level approach to ensure authenticity and prevent malicious activities.

# DATA STORAGE AND QUERYING

In the age of big data, the intricacies of database systems can sometimes be overlooked by those who only view them through a high-level lens. However, at their core, these systems rely on the physical storage of data as bits on various devices, such as magnetic disks or flash storage. The speed at which data can be accessed is largely determined by the characteristics of these devices, with disk access taking significantly longer than memory access.

To navigate the challenges of physical storage, Chapter 10 of this text provides an in-depth overview of storage media, including measures to prevent data loss due to device failure. The chapter also delves into the mapping of records to files and ultimately to bits on a disk.

As many queries only reference a small percentage of records within a file, indices play a crucial role in facilitating speedy data retrieval without the need to scan all records. Chapter 11 explores various types of indices utilized in database systems, with an example provided in the text for human use.

Breaking down complex user queries into smaller, more manageable operations. The text outlines algorithms for implementing individual operations and explains how these operations are executed in unison to process a query.

Given the range of options available for processing a given query, the chapter introduces the concept of query optimization. This process seeks to identify the most cost-effective method for evaluating a query, with varying approaches and costs to consider. In sum, these chapters provide a comprehensive understanding of the essential elements underpinning database systems, from physical storage to query optimization.

## Storage and File Structure

In the world of databases, the focus is often on the high-level models that allow users to access data with ease. Indeed, a database system's ultimate goal is to simplify the process of accessing and managing data, and users should not be unduly burdened with the physical details of the system's implementation.

However, in this chapter and the following ones, we dive beneath the surface to examine the methods used to implement these models and languages. We begin by exploring the fundamental properties of the underlying storage media, including disk and tape systems, before delving into the various data structures that facilitate rapid data access.

By examining different structures and their suitability for specific types of data access, we can make informed decisions about the optimal data structure to utilize based on the expected usage and the physical constraints of the particular machine in question. In short, this chapter serves as a crucial foundation for understanding the inner workings of a database system, and the subsequent chapters will continue to build on this knowledge.

### Overview of Physical Storage Media

Data is the lifeblood of any enterprise, and its storage is paramount. From the fleet-footed cache to the lumbering tape, the range of storage media available to computer systems is varied and vast. Each storage type is categorized by its speed, cost, and reliability, and each has its unique strengths and weaknesses.

At the peak of this hierarchy sits the cache, a fleeting but costly storage medium. The cache's minuscule size is managed by computer system hardware, with its effects considered when designing query processing data structures and algorithms.

Next in line is the main memory, the storage medium that houses data available for processing by the general-purpose machine instructions. Although it can accommodate several gigabytes of data in a personal computer, it is typically inadequate for storing an entire database. Additionally, the contents of the main memory are often lost in the event of a system crash or power failure.

Enter the flash memory, a storage medium that differs from the main memory in its non-volatile nature. Stored data persists even when power is lost, thanks to two types of flash memory, NAND and NOR. NAND flash is more cost-effective and accommodates larger storage capacities for the price. It is widely utilized in portable devices like cameras, music players, and cell phones, and increasingly in laptop computers.

Flash memory is increasingly replacing magnetic disks, serving as solid-state drives that store moderate amounts of data. Its cost per byte is lower than that of main memory, while its larger storage capacity is a boon to system performance. Flash memory is also used in server systems to cache frequently used data, enabling faster access than disks and more storage capacity than main memory.

Magnetic disk storage remains the go-to medium for long-term online storage of data. As the primary medium for storing entire databases, magnetic disks must transfer data to the main memory for processing. Magnetic disks are available in sizes ranging from 80 gigabytes to 1.5 terabytes, with prices beginning at $100 for a 1 terabyte disk. Disk storage survives system crashes and power failures, although disk storage devices themselves may sometimes fail and destroy data.

Optical storage, on the other hand, is exemplified by the compact disk (CD) and the digital video disk (DVD), with optical data storage that is read by a laser. CDs can hold about 700 megabytes of data and have an 80-minute playtime, while DVDs hold between 4.7 and 8.5 gigabytes of data per disk side. Blu-ray DVDs, with 27 gigabytes of capacity per layer, have a double-layer disk capacity of 54 gigabytes.

Tape storage, although slower than disks, is cheaper and well-suited to backup and archival data storage. Tapes can store between 40 and 300 gigabytes of data, making them ideal for exceptionally large data collections such as satellite data, which can easily top hundreds of terabytes or even multiple petabytes.

In conclusion, data storage media is a complex and dynamic field that evolves rapidly. With each medium having its unique benefits, choosing the appropriate storage medium for a specific need is critical.

![Figure 128 - Storage device hierarchy](128.png)

### Magnetic Disk and Flash Storage

Magnetic disks have long been the primary medium for secondary storage. However, as the storage requirements of large applications continue to outpace the growth rate of disk capacities, there has been a growing need for alternative solutions. Enter flash-memory storage, whose sizes have expanded exponentially in recent years, positioning it as a potential competitor to magnetic disk storage in select applications.

In order to better understand the underlying physical characteristics of disks, one must take a closer look at their construction. Disk platters, each having a flat, circular shape, are composed of rigid metal or glass, and possess two surfaces covered with a magnetic material, on which data is recorded. When in use, the platters are spun by a drive motor at a constant high speed, typically ranging from 60 to 120 revolutions per second. To read or write data, a read-write head is positioned just above the platter surface, and the disk surface is divided into tracks and sectors. In today's disks, sector sizes are typically 512 bytes, with around 50,000 to 100,000 tracks per platter, and 1 to 5 platters per disk.

![Figure 129 - Moving head disk mechanism](129.png)

The read-write head, which magnetically stores information on a sector by reversing the direction of magnetization of the magnetic material, moves across the platter to access different tracks. All of the read-write heads on a disk, which may contain many platters, are mounted on a single assembly called a disk arm, and move together, creating the so-called head-disk assembly. The read-write heads being synchronized in this manner means that the ith tracks of all the platters together are referred to as the ith cylinder. In order to increase recording density, the heads are kept as close as possible to the disk surface, typically floating only microns above it.

However, head crashes remain a serious problem. If the head comes into contact with the disk surface, it can scrape off the recording medium, effectively destroying any data present. In older-generation disks, this often led to the medium becoming airborne and coming between the other heads and their platters, causing additional crashes that could result in the failure of the entire disk. Current-generation disk drives utilize a thin film of magnetic metal as the recording medium, making them much less susceptible to failure from head crashes than older oxide-coated disks.

To interface between the computer system and the disk drive unit, a disk controller is employed. This crucial component accepts high-level commands to read or write data and initiates actions such as moving the disk arm to the right track and performing the read or write operation. Disk controllers attach checksums to each sector that is written, which are computed from the data written to the sector. When the sector is read back, the controller computes the checksum again from the retrieved data and compares it with the stored checksum. If an error is detected, the controller will retry the read several times before signaling a failure. Additionally, if a sector is found to be damaged, the controller will remap the sector to a different physical location.

Disks are connected to a computer system via a high-speed interconnection, and there are several interfaces for connecting disks to computers, including SATA and SCSI. However, as the field of data storage technology continues to rapidly evolve, one can be certain that these interfaces will continue to evolve as well.

A clear distinction arises between sequential and random access patterns. In the former, successive requests for data are made in an orderly fashion, with contiguous blocks on the same track or on adjacent tracks being accessed. The first request in such a pattern may require a disk seek, but subsequent requests would either not require a seek or necessitate a seek to an adjacent track, which is much faster than a desire to a farther track.

On the other hand, in a random access pattern, successive requests are for blocks that are randomly located on the disk. Each such request would require a disk seek, and the number of random block accesses that can be processed by a single disk in a second depends on the seek time, which is typically about 100 to 200 accesses per second. Furthermore, since only one block of data is read per seek, the transfer rate is considerably lower with a random access pattern than with a sequential access pattern.

Several techniques have been developed to enhance the speed of access to blocks, including buffering, read-ahead, scheduling, file organization, and nonvolatile write buffers. Buffering involves temporarily storing the blocks read from the disk in an in-memory buffer, which can be used to satisfy future requests. Read-ahead entails reading consecutive blocks from the same track into an in-memory buffer, even if there is no pending request for those blocks. Such read-ahead is useful for sequential access, where it ensures that many blocks are already in memory when they are requested, thereby minimizing the time wasted in disk seeks and rotational latency per block read. Scheduling algorithms attempt to order accesses to tracks in a fashion that increases the number of accesses that can be processed, while file organization involves organizing blocks on disk in a way that corresponds closely to the way data is expected to be accessed.

Finally, nonvolatile write buffers utilize nonvolatile random-access memory (NVRAM) to speed up disk writes dramatically. Battery-backed-up RAM or flash memory can be used to implement NVRAM, and the contents of NVRAM are not lost in a power failure. In update-intensive database applications such as transaction-processing systems, the speed of disk writes heavily influences performance, making nonvolatile write buffers an indispensable tool in boosting performance.

### RAID

As the world's data storage needs continue to skyrocket, with particular emphasis on web, multimedia, and database applications, there has been a pressing demand for faster and more reliable storage solutions. Redundant arrays of independent disks (RAID) are an innovative and powerful technology that has emerged to address these needs.

![Figure 130 - RAID levels](130.png)

By allowing for a large number of disks to be operated in parallel, RAID systems offer unparalleled read/write speeds that are essential for handling data-intensive applications. Performing independent reads and writes in parallel further enhances the system's overall performance.

However, their remarkable reliability may be the most impressive feature of RAID systems. Disk failure is an ever-present danger that can result in the loss of large amounts of valuable data. But RAID technology introduces redundancy, storing extra information that is not ordinarily needed but can be used to rebuild lost information in the event of a disk failure. Mirroring, the most basic RAID technique, duplicates every disk and carries out every write on both disks, so if one disk fails, the data can still be retrieved from the other disk. This redundancy ensures that data are never lost and the mean time to failure is greatly extended.

![Figure 131 - Pattern](131.png)

RAID systems offer an innovative and powerful storage solution that is essential for handling the ever-increasing data storage demands of modern society. By allowing for high-performance parallel reads and writes and introducing redundancy to increase reliability, RAID technology ensures that data are always safe and accessible.

The choice of RAID level is a critical decision that can significantly impact the performance and reliability of a system. With the monetary cost of extra disk storage requirements and the number of I/O operations needed for optimal performance being key factors, the decision of whether to opt for the more popular RAID level 1 or the storage-efficient RAID level 5 is a tough one that requires careful consideration of the unique needs of each application.

As disk-storage capacities continue to grow at an unprecedented rate, the cost per byte has fallen dramatically, making mirroring a more viable option for many existing database applications with moderate storage requirements. However, access speeds have not kept pace with this growth, and the number of I/O operations required per second has skyrocketed, particularly for web application servers. This puts a premium on choosing a RAID level that can deliver the necessary write performance without sacrificing reliability or storage efficiency.

To this end, RAID system designers must make several other crucial decisions, including the number of disks in an array and the number of bits protected by each parity bit. While a higher number of disks can boost data-transfer rates, it also raises the system's cost, while increasing the number of bits protected by a parity bit lowers the space overhead due to parity bits but heightens the risk of data loss if a second disk fails before the first one is repaired.

Hardware is another vital consideration in choosing a RAID implementation, with hardware RAID systems offering several benefits over software RAID. For instance, special-purpose hardware can use nonvolatile RAM to record writes before they are performed, ensuring that incomplete writes are completed in case of power failure. Additionally, good RAID controllers can perform scrubbing to minimize the chance of data loss caused by latent failures or bit rot.

All in all, choosing the right RAID level is a critical decision that requires careful weighing of several factors, including monetary cost, performance requirements, and data safety. With the right combination of RAID level and hardware implementation, data storage and retrieval systems can deliver the high performance and reliability that modern applications demand.

### Tertiary Storage

A peculiar tertiary storage emerges - one that is capable of hosting voluminous amounts of data. Indeed, such data often necessitates the deployment of secondary storage, but when even the latter proves insufficient for the task, tertiary storage provides a solution.

Two prime examples of tertiary storage media come to mind - the magnetic tape and the optical disk. Both serve unique purposes in the storage hierarchy, but in this exposition, we shall focus on the latter.

Compact disks (CDs) have become a popular means of distributing software and multimedia data, including audio and images, and other electronically published content. These disks have a storage capacity ranging from 640 to 700 megabytes, and they can be mass-produced at a low cost. However, digital video disks (DVDs) have replaced CDs in applications requiring higher data volumes. DVD-5 format disks can store up to 4.7 gigabytes of data on a single recording layer, while DVD-9 format disks can store up to 8.5 gigabytes of data on two recording layers. Double-sided disks, such as the DVD-10 and DVD-18 formats, can store even more data - up to 9.4 gigabytes and 17 gigabytes, respectively.

Blu-ray DVDs have set a new benchmark, boasting a capacity of 27 to 54 gigabytes per disk. However, optical disks' seek times are much longer than those of magnetic disks due to their relatively heavier head assembly. They also have lower rotational speeds, although faster CD and DVD drives rotate at speeds comparable to lower-end magnetic disk drives. Optical disks store more data in outside tracks and fewer data in inner tracks, like magnetic disk drives. Their data transfer rates are lower than those of magnetic disks, but they have a transfer rate characteristic of n×, indicating that they can transfer data at n times the standard rate.

Optical disks come in two forms - the record-once version (CD-R, DVD-R, and DVD+R) and the multiple-write version (CD-RW, DVD-RW, DVD+RW, and DVD-RAM). The former is popular for distributing data and archival storage since it cannot be overwritten and is ideal for storing unalterable data, such as audit trails. The latter is also useful for archival purposes.

To achieve even more massive storage capacity, jukeboxes come in handy. These devices store hundreds of optical disks that can be loaded automatically onto one of several drives. The system's aggregate storage capacity can be in the terabytes, with disk load/unload time being much longer than disk access times.

### File Organization

In the realm of database management, the organization of data is crucial for ensuring efficient and effective data retrieval. To this end, files are the basic construct of operating systems and are essential for mapping a database into a series of files that reside permanently on disks. Each file is organized logically as a sequence of records, which are then mapped onto disk blocks.

![Figure 132 - Example](132.png)

In turn, each file is partitioned into fixed-length storage units known as blocks. These blocks serve as the units of storage allocation and data transfer, and most databases use block sizes of 4 to 8 kilobytes by default, although larger block sizes can be specified for specific database applications.

![Figure 133 - File containing instructor records](133.png)

It is important to note that each record must be entirely contained within a single block, and no record should be larger than a block. Although there are large data items such as images that can exceed the block size, these can be handled by storing them separately and including a pointer to the data item in the record. In addition, a relational database has tuples of different sizes. To account for this, we may use several files and store records of only one fixed length in each file. Alternatively, we can structure our files to accommodate multiple lengths for records. However, files of fixed-length records are easier to implement than files of variable-length records.

![Figure 134 - File with record 3 deleted and all records moved](134.png)

![Figure 135 - File with record 3 deleted and ﬁnal record moved](135.png)

In dealing with fixed-length records, let us consider a file of instructor records for a university database as an example. We can allocate the maximum number of bytes that each attribute can hold, which results in an instructor record that is 53 bytes long. However, a simple approach of using the first 53 bytes for the first record, the next 53 bytes for the second record, and so on, would not work. This approach results in records crossing block boundaries, and it becomes difficult to delete records from this structure.

![Figure 136 - File with free list after deletion of records 1, 4, and 6](136.png)

To solve these problems, we allocate only as many records to a block as would fit entirely within the block, leaving any remaining bytes unused. When deleting records, we can move the final record of the file into the space occupied by the deleted record, rather than moving every record following the deleted record. This approach minimizes the number of records that need to be moved and avoids additional block accesses.

![Figure 137 - Representation of variable-length record](137.png)

To manage available space, we introduce an additional structure in the form of a file header that contains information about the file, including the address of the first record whose contents are deleted. By following this approach, we can organize fixed-length records in a way that maximizes efficiency and minimizes errors.

![Figure 138 - Slotted-page structure](138.png)

### Organization of Records in Files

The organization of records in files is a critical aspect of efficient data management. Different techniques are used to store records in files, including heap file organization, sequential file organization, and hashing file organization. These methods enable fast and efficient processing of records, depending on the specific requirements of a given database.

![Figure 139 - Sequential ﬁle for instructor records](139.png)

Sequential file organization, for instance, is designed to facilitate the processing of sorted records based on some search key. To achieve this, records are stored physically in search-key order, and chains of pointers are used to link them together. 

![Figure 141 - Example](141.png)

While this organization permits fast retrieval of records in search-key order, it can be challenging to maintain physical sequential order as records are inserted and deleted. To address this issue, pointer chains are utilized for record deletion, while specific rules guide the insertion of new records.

![Figure 140 - Sequential ﬁle after an insertion](140.png)

![Figure 142 - The department relation](142.png)

![Figure 143 - The instructor relation](143.png)

Multitable clustering file organization is another technique used to store records of different relations in the same file. In this approach, related records of different relations are stored on the same block, allowing fast retrieval of related records from different relations in a single I/O operation. Although this simple file structure is well suited to small database systems such as those found in embedded systems or portable devices, more complex file structures may be required for larger databases to ensure optimal performance.

Understanding the various techniques for organizing records in files is vital for the effective management of database systems. These techniques enable fast and efficient processing of records, depending on the specific requirements of a given database.

![Figure 144 - Multitable clustering ﬁle structure](144.png)

![Figure 145 - Multitable clustering ﬁle structure with pointer chains](145.png)

### Data-Dictionary Storage

The storage of metadata, also known as "data about data", is crucial for any relational database system. This includes information about the schema of relations, views, integrity constraints, and authorized users. In addition, statistical data such as the number of tuples and storage methods for each relation may also be stored. The data dictionary, or system catalog, is the structure that stores all of this important metadata.

To ensure efficient access to system data, it is recommended to store metadata as relations within the database itself. However, the exact representation of this metadata must be determined by the system designers. One possible representation is shown in the Figure, which is not in first normal form but is likely to be more efficient for access.

When retrieving records from a relation, the database system must consult the related metadata to find the location and storage organization of the relation. It is important to note that the storage organization and location of the relation metadata itself must be recorded elsewhere for easy retrieval.

In essence, the metadata stored in the data dictionary constitutes a miniature database that serves as the backbone for the entire relational database system.

![Figure 146 - Relational schema representing system metadata](146.png)

### Database Buffer

In the realm of database systems, the maximization of efficiency is the ultimate goal. One of the most crucial objectives in achieving this is to minimize the number of block transfers between the memory and disk. The method by which we can accomplish this is to retain as many blocks as possible in the main memory. The intention is to heighten the likelihood that when a block is accessed, it already exists in the main memory, and as a result, no disk access is necessary.

The space available in the main memory for the storage of blocks must be allocated wisely, as it is not feasible to keep all blocks in the main memory. The buffer, which is part of the main memory available for the storage of copies of disk blocks, is responsible for the allocation of buffer space, and the subsystem managing it is known as the buffer manager. Every block has a copy on disk, but the copy on disk may be an older version than the one in the buffer.

When a program in the database system requests a block from the disk, it makes a call to the buffer manager. If the block already exists in the buffer, the buffer manager delivers the address of the block in the main memory to the requester. However, if the block is not in the buffer, the buffer manager must first allocate space in the buffer for the block. To make room for the new block, the buffer manager may have to discard another block. If the discarded block has been modified since it was last written to disk, it must be written back to the disk. The buffer manager then reads the requested block from the disk to the buffer and delivers the address of the block in the main memory to the requester. The buffer manager's internal activities are imperceptible to the programs that request disk-block access.

To many, the buffer manager appears to be nothing more than a virtual-memory manager, much like those found in most operating systems. However, the size of the database could exceed the hardware address space of a machine. Furthermore, the buffer manager must employ more sophisticated methods than typical virtual-memory management schemes to serve the database system effectively. These include buffer replacement strategies, pinned blocks, and forced output of blocks.

![Figure 147 - Procedure for computing join](147.png)

The buffer replacement policy's primary goal is to reduce access to the disk by replacing blocks in the buffer. Since it is not feasible to forecast which blocks will be referenced by general-purpose programs, operating systems use past block-reference patterns as a predictor of future references. In contrast, database systems may have information concerning at least the short-term future because a user request to the database system involves multiple steps.

The toss-immediate strategy is an example of a buffer management strategy. It instructs the buffer manager to free the space taken up by an instructor block as soon as the final tuple has been processed, even though the block has been used recently. Another example is the read-ahead strategy, where the buffer manager reads blocks into the buffer in anticipation of future block accesses. The buffer manager then removes the blocks from the buffer once they are no longer required. These approaches, which utilize information about future block access, allow us to improve the LRU strategy.

## Indexing and Hashing

In the vast realm of databases, the efficiency of queries that access only a fraction of the records is crucial. Why waste precious time and resources sifting through irrelevant tuples when we can swiftly locate the desired ones? Queries such as "Find all instructors in the Physics department" or "Find the total number of credits earned by the student with ID 22201" only require a small subset of records to be accessed, rendering a traditional read of the entire relation impractical. Therefore, additional structures, such as indexing and hashing, are implemented to enhance the system's performance and enable direct access to the desired records.

### Basic Concepts

In the world of database systems, indices play a pivotal role in efficiently accessing data. An index is much like the index in a textbook, allowing us to quickly locate the pages containing the desired information. Similarly, a database index allows us to quickly find the disk block containing the data record that matches our search criteria.

However, maintaining a sorted list of data values, such as a list of student IDs, can become unwieldy in large databases with thousands of entries. This is where sophisticated indexing techniques come into play, such as ordered indexing and hashing.

Each indexing technique has its own strengths and weaknesses and must be evaluated based on a variety of factors, including access types, access time, insertion time, deletion time, and space overhead. While no one technique is universally superior, each is best suited to specific database applications.

It is also common to have multiple indices for a single file, such as indices for author, subject, and title searches. These attributes used to look up records in a file are known as search keys.

Database indexing is a complex and nuanced one, with a variety of techniques available to suit different needs. Whether using ordered indices or hash indices, it is crucial to consider the various factors involved in evaluating the effectiveness of each technique and to carefully choose the search keys for each index to ensure efficient and accurate data access.

### Ordered Indices

The efficient retrieval of records is a key concern. To facilitate this process, an index structure can be employed. Such a structure is associated with a specific search key and stores the values of the search keys in sorted order. The ordered index, similar to a book's index, enables fast random access to records, and each search key is associated with the records that contain it.

In some cases, the records themselves may be stored in some sorted order, and a file may have multiple indices on different search keys. If the file is sequentially ordered, a clustering index is used to define the sequential order of the file. Such an index is also called a primary index and can be built on any search key, not necessarily a primary key.

Indices whose search key specifies an order different from the sequential order of the file are called non-clustering indices or secondary indices. Dense indices and sparse indices are two types of ordered indices. A dense index contains an index entry for every search-key value in the file, while a sparse index contains entries for only some of the search-key values.

![Figure 148 - Sequential ﬁle for instructor records](148.png)

A search in a dense index is quicker as each index record contains a search-key value and a pointer to the first data record with that search-key value. Sparse indices, on the other hand, can only be used if the relation is stored in the sorted order of the search key. In such cases, each index entry contains a search-key value and a pointer to the first data record with that search-key value. To locate a record, we find the index entry with the largest search-key value that is less than or equal to the search-key value for which we are looking.

![Figure 149 - Dense index](149.png)

The use of ordered indices is crucial for applications that require both sequential processing of an entire file and random access to individual records. By utilizing such structures, we can expedite record retrieval and optimize database performance.

![Figure 150 - Sparse index](150.png)

![Figure 151 - Dense index with search key dept name](151.png)

Even the most efficient search mechanisms can be brought to their knees by the sheer size of an index file. Such files, stored as sequential files on disk, can become unwieldy and time-consuming to search as they grow into the gigabyte range. This can lead to frustration for users who require quick access to data.

Enter the multilevel index - a tool that promises to make searching large index files a breeze. By constructing a sparse outer index on top of an inner index, a multilevel index allows users to perform a search using just one index block read, as opposed to the 14 required by binary search.

But what happens when even the outer index grows too large to fit into the main memory? No problem - simply create another level of the index. In fact, the process can be repeated as many times as necessary to accommodate even the largest index files.

![Figure 152 - Two-level sparse index](152.png)

Of course, every index must be updated whenever a record is inserted, deleted, or updated in the file. This can be modeled as a deletion of the old record followed by an insertion of the new value, resulting in an index deletion followed by an index insertion. But with algorithms designed for single-level indices, the process of updating a multilevel index need not be a headache.

So whether you're managing a small-scale database or one that's millions of records strong, the multilevel index is a tool you'll want to have in your arsenal. Its power lies in its ability to perform fast and efficient searches, making it a must-have for any serious data manager.

The concept of secondary indices plays a critical role in the efficient retrieval of records based on search-key values. A secondary index is considered dense, meaning that every search-key value has a corresponding index entry, along with a pointer to each record in the file. This stands in contrast to a clustering index, which can afford to be sparse, as it is always possible to sequentially access a portion of the file to locate records with intermediate search-key values.

When a secondary index is created on a candidate key, it closely resembles a dense clustering index. However, if the search key of a secondary index is not a candidate key, then it must contain pointers to all records, as the records are not ordered by the search key of the secondary index. In this scenario, an extra level of indirection is used to implement the secondary index, with pointers directed to a bucket containing pointers to the file.

![Figure 153 - Secondary index on instructor ﬁle, on noncandidate key salary](153.png)

Indices on multiple keys, known as composite search keys, offer further potential for database optimization. An ordered index on a composite key allows for efficient retrieval of records based on multiple attributes, using lexicographic ordering to establish the order of search-key values.

While secondary indices can significantly improve query performance, they also impose a substantial overhead on database modification. Therefore, the decision to implement secondary indices is made on the basis of an estimate of the relative frequency of queries and modifications.

### B+-Tree Index Files

As we delve into the world of database indexing, we encounter the well-known limitation of the index-sequential file organization: its performance degrades as the file size grows. Frequent file reorganization can alleviate this, but it's an undesirable solution.

Enter the B+-tree index structure, the most widely used indexing structure that maintains efficiency despite data insertion and deletion. It takes the form of a balanced tree where every path from the root to a leaf is of equal length. Each non-leaf node has between n/2 and n children, where n is a fixed value for a particular tree.

![Figure 154 - Typical node of a B+-tree](154.png)

![Figure 155 - A leaf node for instructor B+-tree index (n = 4)](155.png)

Despite imposing performance and space overhead on insertion and deletion, the B+-tree structure provides acceptable results even for frequently modified files as the cost of file reorganization is avoided. And with nodes capable of holding up to half-empty children, wasted space is a small price to pay for the performance benefits of the B+-tree structure.

![Figure 156 - B+-tree for instructor ﬁle (n = 4)](156.png)

A B+-tree index is a multilevel index, unlike the multilevel index-sequential file, and the structure of its nodes differs as well. Each node can contain up to n-1 search-key values and n pointers, which are kept in sorted order. The ranges of values in each leaf do not overlap, except for duplicate search-key values, and every search-key value must appear in some leaf node.

![Figure 157 - B+-tree for instructor ﬁle with n = 6](57.png)

![Figure 158 - Querying a B+-tree](158.png)

With a linear order of leaves based on their search-key values, the pointer Pn is used to chain the leaf nodes together in search-key order, allowing for efficient sequential processing of the file. Non leaf nodes of the B+-tree form a multilevel index on the leaf nodes, with a similar structure as the leaf nodes, but with all pointers pointing to tree nodes instead.

The B+-tree index structure provides a dynamic indexing solution that maintains its efficiency despite data insertion and deletion. Its multilevel structure allows for efficient sequential processing of the file, with acceptable performance and space overhead for frequently modified files. As we look toward the future of database indexing, the B+-tree structure remains a reliable and widely used option.

The B+-tree structure stands apart from its in-memory tree brethren. While binary trees consist of small nodes, each having no more than two pointers, the nodes in B+ trees are comparably large - often an entire disk block - and can contain a considerable number of pointers. As such, B, trees adopt a shape that is the inverse of the tall, skinny binary tree, instead opting for a short, wide structure.

![Figure 159 - Split of leaf node on insertion of "Adam"](159.png)

However, despite their differences in size, both B+ trees and binary trees are useful for indexing records in a file, and the effectiveness of their lookup operations is contingent on the number of records contained therein. In a balanced binary tree, for instance, the length of the path for a lookup would be proportional to the logarithm of the number of records in the indexed file. For a file with one million records, this would necessitate around 20 node accesses.

![Figure 160 - Insertion of “Adams” into the B+-tree](160.png)

![Figure 161 - Insertion of “Lamport” into the B+-tree](161.png)

If each node were located on a different disk block, 20 block reads would be required to process a lookup. This is in stark contrast to the mere four block reads needed for the B+-tree, where nodes are more capacious and can hold more pointers. The difference in required block reads may seem trivial, but the time cost of each read, coupled with the need for disk arm seeks, compounds the disparity. Such a read with a disk arm seeks can take upwards of 10 milliseconds on a typical disk, which is no small delay in the realm of computing.

![Figure 162 - Insertion of entry in a B+-tree](162.png)

Updating records in a relation can be challenging, especially when indices are involved. A record update can be modeled as a deletion of the old record followed by an insertion of the updated record. Insertions and deletions can be more involved than lookups since they may necessitate node splitting, where a node is divided in two, or node coalescing, where two nodes are combined. In addition, when a node is split or combined, the balance of the tree must be maintained.

![Figure 163 - Deletion of “Singh” and “Wu” from the B+-tree](163.png)

When inserting a record into a B+-tree, one must first find the leaf node that should contain the new record. After doing so, an entry - consisting of the search-key value and record pointer pair - can be added to the node in such a way that the search keys remain sorted. Conversely, when deleting a record, the node containing the entry to be deleted must first be found, and the entry can then be removed. The remaining entries in the node to the right of the deleted entry are then shifted left by one position so that there are no gaps in the entries.

![Figure 164 - Deletion of “Gold” from the B+-tree](164.png)

Node splitting can occur when a node becomes too large to hold its contents, and the example given in the text illustrates this. If a record with the name "Adams" is inserted into a B+-tree, and the leaf node containing "Brandt," "Califieri," and "Crick" does not have enough space to accommodate it, the node must be split into two separate nodes. The first n/2 search-key values are kept in the existing node, while the remaining search-key values are added to the newly created node. The new leaf node is then inserted into the B+-tree structure by adding an entry - consisting of the smallest search-key value and a pointer to the new node - into the parent of the split node.

Overall, the updating of records in a B+-tree structure is complex, as it involves a delicate balance of node splitting, node coalescing, and parent-node insertion, all with an eye toward maintaining the overall balance of the tree.

The importance of efficient and speedy search operations cannot be overstated. Enter the B+-tree, a ubiquitous index structure used to optimize search operations on large datasets. However, as with any system, there are limitations to be addressed, such as the handling of nonunified search keys.

In situations where a relation can contain multiple records with the same search key value or a nonunified search key, the process of deleting a specific record can prove arduous. With a large number of entries to sift through, even spanning multiple leaf nodes, finding the corresponding entry for deletion can be a time-consuming process. To combat this, most database systems utilize a composite search key that contains the original search key and another attribute, unique to each record, creating a unique search key for each record. This extra attribute, known as the unifier attribute, enables the database to locate and delete the record efficiently with a single traversal from root to leaf.

While nonunified search keys pose challenges, an alternative to the traditional storage method exists, where each key value is stored only once in the tree, with a bucket or list of record pointers used to handle nonunified search keys. This approach is more space-efficient, but implementation comes with extra complexities, such as variable-sized buckets, fetching records across multiple blocks, and inefficient deletion operations.

![Figure 165 - Procedure for computing join](165.png)

Despite the complexities, B+-trees remain a popular choice for index structures in database management systems, with their low I/O operation costs for insertion and deletion. The worst-case complexity of these operations is proportional to the height of the B+-tree, and with a fanout of 100, operations result in fewer I/O operations than the worst-case bounds. In addition, with large memory sizes being commonplace, most non-leaf nodes are already in the database buffer when they are accessed, and only one or two I/O operations are required for a lookup.

Furthermore, with random insertions, B+-tree nodes can be expected to be more than two-thirds full on average, and even in the case of sorted insertions, they are only half full. The B+-tree's capabilities and limitations must be carefully considered when implementing a database management system, but their efficiency and speed make them a reliable and often utilized tool in large-scale data management.

### B+-Tree Extensions

The use of the B+-tree index structure has become a staple for efficient and organized file storage. While index-sequential file organization can be riddled with performance issues as the file grows, the B+-tree structure provides a solution to the degradation of index lookups and actual record storage. By utilizing the leaf level of the B+-tree as an organizer for records in a file, rather than just as an index, we can avoid the issue of storing pointers to records and instead store the records themselves.

![Figure 166 - B+-tree ﬁle organization](166.png)

Inserting and deleting records in a B+-tree file organization follows the same principles as in a B+-tree index. To insert a record with a given key value, the system locates the block that should contain the record by searching the B+-tree for the largest key that is less than or equal to the given value. If the block has enough free space, the record is stored in the block. Otherwise, the block is split and the records are redistributed to create space for the new record. Deleting a record works similarly, as the record is removed from its block and the non-leaf nodes of the B+-tree are updated.

To improve space utilization in a B+-tree, we can involve more sibling nodes in redistribution during splits and merges. By redistributing entries between adjacent nodes during insertion or deletion, we can ensure that each node contains at least a certain number of entries. However, as more sibling nodes are involved in redistribution, the cost of updating becomes higher.

It is important to note that in a B+-tree index or file organization, leaf nodes that are adjacent to each other in the tree may not be located adjacent to each other on disk. As such, sequential access to the file may become increasingly lost as insertions and deletions occur. In such cases, an index rebuild may be required to restore sequentiality.

Finally, B+-tree file organizations can be used to store large objects, such as SQL clobs and blobs, which may be larger than a disk block. By splitting these objects into smaller records that are organized in a B+-tree file organization, we can efficiently store and access these large objects.

As we delve into the world of indexing, we come across the B-Tree and the B+-Tree - two distinct data structures that serve a common purpose. The B-Tree stands out from its sibling in that it avoids the redundant storage of search-key values, a trait that could potentially reduce the number of nodes in an index.

![Figure 167 - Procedure for computing join](167.png)

As we scrutinize the Figure above, we notice that the B-Tree, unlike the B+-Tree, limits the number of times a search-key value appears. This constraint brings about the need for additional pointer fields in nonleaf nodes that point to file records or buckets associated with a search key.

Despite the growing trend in using B-Tree and B+-Tree interchangeably, this book adheres to the conventional definition of the two data structures to prevent any confusion. A generalized B-Tree is presented in Figure below, with leaf nodes identical to that of the B+-Tree.

![Figure 168 - Typical nodes of a B-tree. (a) Leaf node. (b) Nonleaf node](168.png)

The number of nodes accessed during a lookup in a B-Tree varies based on the location of the search key. In contrast to the B+-Tree, a B-Tree could present the desired value before reaching a leaf node. Nevertheless, the advantages of finding certain values early on are insignificant, given that B-Tree's nonleaf nodes contain fewer search keys, leading to a smaller fanout and a greater depth than that of its cousin.

Deleting entries in a B-Tree is more complicated than in a B+-Tree, given that the entry could appear in nonleaf nodes. On the other hand, inserting values in a B-Tree is a relatively simple process. However, when it comes to large indices, the space advantages of B-Trees are trivial, making B+-Tree the preferred choice for most database-system implementations.

As we tread further into the world of indexing, it's worth noting that the rise of flash memory has revolutionized data storage, and its impact on the index structure is undeniable. With the B+-Tree index structure compatible with flash memory storage, faster access speeds are guaranteed, and lookup times are reduced to a mere microsecond, giving magnetic disk storage a run for its money.

### Multiple-Key Access

The use of multiple indices is a strategy that can greatly improve query processing efficiency for certain types of queries. In particular, when queries involve multiple attributes, an index built on a composite search key can provide a significant advantage over the use of single-key indices.

However, the effectiveness of this strategy can depend heavily on the specific query and data characteristics. In some cases, the use of multiple indices can result in a large number of pointers being scanned to produce a small result, leading to poor query performance. To address this issue, specialized index structures such as bitmap indices and R-trees have been developed to speed up the intersection and comparison operations involved in query processing.

Another optimization technique is the use of covering indices, which store the values of some attributes along with the pointers to the record. This technique can allow certain queries to be answered using just the index, without accessing the actual records. While this technique can improve query processing efficiency, it also increases the size of the search key, leading to increased storage requirements.

Overall, the use of multiple indices and specialized index structures represents a powerful tool in the arsenal of database system designers, but it must be applied judiciously and with careful consideration of the specific query and data characteristics involved.

### Static Hashing

Hashing has emerged as a technique that provides a way of constructing indices and avoids accessing index structures or employing binary search, thereby reducing the number of input/output (I/O) operations. However, not all hash functions are created equal. To ensure an even distribution of records across buckets, an ideal hash function should distribute search keys uniformly across all buckets and appear random, regardless of any externally visible ordering on the search-key values.

![Figure 169 - Hash organization of instructor ﬁle, with dept name as the key](169.png)

To illustrate this point, consider the case of the instructor file, where the search key is the department name. If a simple hash function is employed, which maps names beginning with the ith letter of the alphabet to the ith bucket, the distribution will not be uniform due to the imbalance in the number of names beginning with certain letters.

![Figure 170 - Overﬂow chaining in a hash structure](170.png)

On the other hand, a hash function based on the search key salary, which divides the values into 10 ranges, provides a uniform distribution but is not random, as records with certain salaries are more common than others.

Therefore, it is important to choose a hash function carefully, taking into account the specific characteristics of the search keys and the size of the file. Typical hash functions operate on the binary representation of characters in the search key and employ mathematical operations to ensure an even distribution of records across buckets. By selecting an appropriate hash function, file organization can be optimized, reducing the number of I/O operations required and improving overall system performance.

![Figure 171 - Hash index on search key ID of instructor ﬁle](171.png)

### Dynamic Hashing

The issue of fixed bucket addresses presents a grave challenge when utilizing the static hashing technique. Databases, as we know, tend to grow in size over time. This, however, poses a problem for static hashing, and when dealing with such databases, we have three possible options.

Firstly, we may choose to base our hash function on the current size of the file. However, this option results in a loss of performance as the database continues to expand. Secondly, we can opt for a hash function based on the anticipated size of the file at some point in the future. Although this approach avoids a decline in performance, it may result in a substantial initial wastage of space.

Lastly, we may periodically reorganize the hash structure to accommodate the growth of the database. This, however, is a massive and time-consuming operation, requiring the choice of a new hash function, the recomputation of the hash function on every record in the file, and the generation of new bucket assignments. Moreover, it is necessary to prevent access to the file during this reorganization process.

Fortunately, several dynamic hashing techniques, including extendable hashing, allow for the hash function to be modified dynamically to cope with the growth or shrinkage of the database. With extendable hashing, we can split and coalesce buckets as the database expands or contracts, thus retaining space efficiency. The reorganization process in this case is performed on only one bucket at a time, ensuring that the resulting performance overhead is acceptably low.

To achieve this, we select a hash function h that generates values over a relatively large range, typically b-bit binary integers, with b being 32 in most cases. Instead of creating a bucket for each hash value, we create buckets on demand, as records are inserted into the file. At any point, we use i bits, where 0 ≤ i ≤ b, to locate the correct bucket for a record.

![Figure 172 - General extendable hash structure](172.png)

The general extendable hash structure, as illustrated in the Figure above, shows the i bits required to determine the correct bucket for a given record. The integer associated with each bucket represents the length of the common hash prefix shared by all entries that point to that bucket.

![Figure 173 - Hash function for dept name](173.png)

To perform a lookup, insertion, or deletion on an extendable hash structure, the system takes the first i high-order bits of the hash value and follows the corresponding table entry for this bit string, thereby locating the bucket containing the search-key value. If the bucket is full, it must be split and the records redistributed. To determine whether it needs to increase the number of bits used, the system checks whether i is equal to ij.

If i is equal to ij, only one entry in the bucket address table points to the bucket. In this case, the system increases the size of the bucket address table by considering an additional bit of the hash value, doubling the size of the table, and allocating a new bucket. It then rehashes each record in the original bucket and, depending on the first i bits, either keep it in the original bucket or assigns it to the newly created bucket.

Extendable hashing offers an efficient and dynamic solution for databases that grow or shrink in size.

In the pursuit of efficient data storage and retrieval, computer scientists have long been on the lookout for the most optimal hashing techniques. Among the contenders for the top spot is extendable hashing, a dynamic hashing technique that promises optimal performance without the typical space overhead associated with other hashing techniques.

![Figure 174 - Initial extendable hash structure](174.png)

![Figure 175 - Hash structure after three insertions](175.png)

In a recent demonstration of the power of extendable hashing, the illustrious instructor file in Figure 176 was used as a test case to illustrate the operation of insertion. Utilizing the 32-bit hash values in Figure 177, and assuming an empty file as in Figure 178, records were inserted one by one, to showcase all the features of extendable hashing in a small structure.

![Figure 176 - Hash structure after four insertions](176.png)

![Figure 177 - Hash structure after six insertions](177.png)

![Figure 178 - Hash structure after seven insertions](178.png)

In the interest of simplicity, it was assumed that each bucket could hold only two records. The first two records were inserted without incident, but when the third record was introduced, it became evident that the bucket was already full.

![Figure 179 - Hash structure after eleven insertions](179.png)

![Figure 180 - Extendable hash structure for the instructor ﬁle](180.png)

To accommodate the overflow, the number of bits used in the hash value was increased, and the bucket was split, with the new bucket holding records whose search key had a hash value beginning with 1. As the file grew, buckets continued to be allocated dynamically, without the need for any buckets to be reserved for future growth.

While extendable hashing does involve an additional level of indirection in the lookup process, the advantages of its dynamic allocation and optimal performance make it a highly attractive technique for data storage and retrieval. Though it requires a more complex implementation than other hashing techniques, the bibliographical notes provide more detailed descriptions of extendable hashing and alternative dynamic hashing techniques, such as linear hashing, that avoid the extra level of indirection.

### Comparison of Ordered Indexing and Hashing

The choice of file organization and indexing technique can make all the difference. Should one use ordered indexing or hashing? The answer is not so straightforward, as each technique has its advantages and disadvantages depending on the situation at hand.

If a system's queries primarily involve searching for a specific value, a hashing scheme may be preferable. With hashing, the average lookup time is constant and independent of the size of the database. In contrast, an ordered-index lookup requires time proportional to the logarithm of the number of values in r for the given attribute. However, the worst-case lookup time for hashing is proportional to the number of values in r for the attribute, whereas the worst-case lookup time for ordered indexing is proportional to the logarithm of the number of values in r. Nevertheless, as worst-case scenarios are unlikely to occur with hashing, it remains the preferred method.

On the other hand, if the queries involve a range of values, ordered-index techniques are preferable. When executing a range query with an ordered index, the system performs a lookup on the first value in the range, then follows the pointer chain in the index to read the next bucket in order until it reaches the end of the range. With hashing, it is difficult to determine the next bucket that must be examined, as a good hash function assigns values randomly to buckets. Thus, the values in the specified range are likely to be scattered across many or all of the buckets, necessitating the reading of all the buckets to find the required search keys.

In general, the decision to use ordered indexing or hashing depends on several factors. The cost of periodic reorganization of the index or hash organization, the relative frequency of insertion and deletion, the desired optimization of average access time versus increasing worst-case access time, and the types of queries that users are likely to pose all come into play. Ultimately, the choice between these two techniques must be made based on the expected type of query. However, in cases where it is not known in advance whether range queries will be infrequent or not, it is usually best to choose ordered indexing, unless the database is temporary and no range queries will be performed.

### Bitmap Indices

After delving into the depths of database indexing, we come across the specialized world of Bitmap Indices. These unique indices offer a streamlined approach to querying multiple keys within a given relation. While each bitmap index is built on a single key, the sequential numbering of records within the relation paves the way for efficient retrieval of information.

To illustrate the usefulness of bitmap indices, let us consider a relation with an attribute that can only take on a small number of values. A prime example of this would be the attribute "gender" in a relation containing instructor information. In such a scenario, creating a bitmap index for each possible value of the attribute allows for quick identification of the relevant records.

![Figure 181 - Bitmap indices on relation instructor info](181.png)

But the true power of bitmap indices shines through when there are selections on multiple keys. By creating bitmap indices on multiple attributes, we can perform queries that require satisfying multiple conditions. The intersection of the resulting bitmaps provides the necessary information for the query, enabling us to bypass access to the entire relation.

In addition to their query prowess, bitmap indices also offer a space-saving advantage. With each bitmap consisting of a mere array of bits, the size occupied by bitmap indices is typically less than 1% of the relation size. And when an attribute can only take on a limited number of values, the bitmap index size shrinks even further, occupying a measly 1% of the relation size.

The flexibility and efficiency of bitmap indices make them a valuable tool for data analysis. By leveraging their unique structure, we can retrieve information and count the number of tuples satisfying a given selection, all without even accessing the relation. So the next time you find yourself knee-deep in database indexing, consider the power of bitmap indices to streamline your queries and simplify your data analysis.

### Index Deﬁnition in SQL

The SQL standard offers no provisions for the user or administrator to regulate the creation and maintenance of indices in the database system. While indices are not essential for data accuracy, they play a pivotal role in efficient transaction processing, including updates and queries. Moreover, indices facilitate the enforcement of integrity constraints.

In theory, a database system could automate the process of determining which indices to create. However, due to the spatial costs associated with indices and their impact on update processing, it is challenging to automatically make the right choices. As a result, most SQL implementations provide programmers with control over index creation and deletion via data definition language (DDL) commands.

The syntax of these commands is illustrated next. While widely used and supported by various database systems, it is not part of the SQL standard. The SQL standard restricts itself to the logical database schema and does not support the physical database schema's management.

Creating an index requires the "create index" command with the following form: "create index  on  ()". The attribute list consists of the attributes of the relations that constitute the search key for the index.

To create an index named "dept index" on the instructor relation with "dept name" as the search key, we would write "create index dept index on the instructor (dept name)". If we wish to declare that the search key is a candidate key, we add the attribute "unique" to the index definition. The command "create unique index dept index on the instructor (dept name)" would indicate that "dept name" is a candidate key for "instructor." However, it is unlikely that this is what we would want for our university database. If "dept name" is not a candidate key at the time of the "create unique index" command, the system will display an error message, and the index creation attempt will fail. If the index-creation attempt succeeds, any subsequent attempt to insert a tuple that violates the key declaration will fail. It is worth noting that the "unique" feature is redundant if the database system supports the unique declaration of the SQL standard.

Some database systems allow the specification of the type of index to be used, such as B+-tree or hashing. Additionally, certain database systems permit one of the indices on a relation to be declared as "clustered." The system then stores the relation sorted by the search-key of the clustered index.

Finally, to drop an index, the "drop index" command takes the form "drop index ." The index name we specified when creating the index is required for this command.

## Query Processing

The intricate process of extracting data from a database, known as query processing, involves a multitude of activities. Among these activities are the translation of high-level database language queries into expressions that can be utilized at the physical level of the file system, a myriad of query-optimizing transformations, and ultimately, the evaluation of queries. The complex and dynamic nature of query processing necessitates a careful and deliberate approach, requiring a thorough understanding of the underlying database architecture and the nuances of query optimization.

### Overview

The process of query processing is a complex and intricate task, involving several steps that culminate in the retrieval of data from a database. These steps are illustrated in the Figure and include parsing and translation, optimization, and evaluation. Before the commencement of query processing, the system must first convert the query into a format that is suitable for internal use. While SQL is well-suited for human consumption, it is unsuitable as an internal representation of a query. Therefore, a more useful format is one based on extended relational algebra.

![Figure 182 - Steps in query processing](182.png)

The initial step in query processing is the translation of the query into its internal format, a process akin to that performed by a compiler's parser. During the translation process, the parser checks the syntax of the query, confirms that the relation names referenced in the query are indeed present in the database, and so on. The result of this process is a parse-tree representation of the query, which is subsequently converted into a relational-algebra expression. If the query is defined in terms of a view, the translation phase replaces all references to the view with the relational-algebra expression that defines the view.

![Figure 183 - Example](183.png)

While a query can be expressed in various ways, there are typically multiple methods for computing the answer. The relational-algebra representation of a query partially specifies how the query is evaluated, but several different algorithms can be used to evaluate the expression. The process of fully specifying how to evaluate a query involves not only providing the relational-algebra expression but also annotating it with instructions on how to evaluate each operation, a process known as query optimization. A sequence of primitive operations that can be used to evaluate a query is a query-execution plan or query-evaluation plan.

Different evaluation plans for the same query can have different costs, and it is the responsibility of the system to construct a query-evaluation plan that minimizes the cost of query evaluation. This task, known as query optimization, is discussed in detail in Chapter 13. Once the query plan is chosen, the query is evaluated, and the result of the query is output.

![Figure 184 - A query-evaluation plan](184.png)

Although the precise sequence of steps involved in query processing can vary among databases, the concepts described here form the foundation of query processing in databases. To optimize a query, the query optimizer must have knowledge of the cost of each operation. While it is difficult to compute the exact cost, it is possible to estimate the execution cost for each operation. In this chapter, we delve into how individual operations are evaluated in a query plan and how their costs can be estimated. Additionally, we explore how pipelined operations can be used to coordinate the execution of multiple operations and avoid the writing of intermediate results to disk.

### Measures of Query Cost

Optimizing query evaluation plans in a database system is a crucial task that involves comparing and choosing among several alternatives based on their estimated costs. To estimate the cost of an evaluation plan, it is necessary to first estimate the cost of individual operations and then combine them to get the total cost of the plan.

The cost of query evaluation is measured in terms of various resources such as disk accesses, CPU time, and communication costs in a distributed system. However, in large databases, the cost of accessing data from disk is usually the most significant as disk accesses are inherently slower than in-memory operations. Therefore, disk activity is expected to dominate the total query execution time, and the number of block transfers and disk seeks are used to estimate the cost of a query evaluation plan.

To further refine the cost estimates, it is necessary to distinguish between block reads and writes as the latter are typically twice as expensive as reads. Nevertheless, such details are often ignored for simplicity, and buffer size in main memory is used to estimate the cost of various algorithms. In the best case, all data can be read into buffers, and the disk is not accessed again. However, in the worst case, only a few blocks of data can be stored in the buffer, and the cost estimates are based on such pessimistic assumptions.

In addition, the response time for a query evaluation plan is a critical measure of its cost. Unfortunately, estimating response time is challenging as it depends on multiple factors such as the contents of the buffer when the query begins execution and the distribution of accesses among multiple disks. As a result, rather than minimizing response time, optimizers focus on minimizing the total resource consumption of the query plan.

Estimating the cost of query evaluation plans involves considering various factors such as disk accesses, CPU time, and communication costs. Although the response time is an essential measure of cost, estimating it is challenging, and optimizers instead focus on minimizing total resource consumption.

### Selection Operation

The file scan reigns supreme as the most fundamental operator for accessing data. It functions as a search algorithm that relentlessly seeks out and retrieves records that meet the conditions specified in a selection. In the case of relational systems, the file scan allows for the entire relation to be read when it is stored in a single, dedicated file.

When it comes to implementing a selection operation on a relation consisting of tuples stored together in one file, there are various algorithms to consider. The linear search algorithm, for instance, entails scanning each file block and testing all records for compatibility with the selection condition. Although it may not be the speediest method of implementing a selection, the linear search algorithm can be applied to any file, regardless of the ordering of the file, the availability of indices, or the nature of the selection operation.

On the other hand, other selection algorithms that exist tend to be faster than linear search but are not universally applicable. Among these algorithms, some use index structures, which are referred to as access paths. Such structures provide a pathway through which data can be located and accessed, with the selection predicate guiding the choice of the index used in processing the query.

For instance, a primary index (also known as a clustering index) is an index that allows the records of a file to be read in an order that corresponds to the physical order in the file. When an equality comparison on a key attribute with a primary index is made, the index can be used to retrieve a single record that satisfies the corresponding equality condition. Cost estimates are shown in the Figure below:

![Figure 185 - Cost estimates for selection algorithms](185.png)

Additionally, there are cases where multiple records may need to be fetched, such as when a primary index is used to retrieve multiple records if the selection condition specifies an equality comparison on a non-key attribute. In such instances, the records must be stored consecutively in the file since the file is sorted on the search key.

Selections specifying an equality condition can also use a secondary index. If the equality condition is on a key, this strategy can retrieve a single record. However, if the indexing field is not a key, multiple records may be retrieved. In this second case, each record may be resident on a different block, which could result in one I/O operation per retrieved record, with each I/O operation requiring a seek and a block transfer. The worst-case time cost, in this case, is dependent on several factors, and could even exceed that of linear search if a large number of records are retrieved.

It is worth noting that when records are stored in a B+-tree file organization or other file organizations that may require relocation of records, secondary indices usually do not store pointers to the records. Instead, they store the values of the attributes used as the search key in a B+-tree file organization. Accessing a record through such a secondary index is more expensive, as it requires searching the secondary index to find the primary index search-key values, and then looking up the records in the primary index. Cost formulae described for secondary indices must be modified accordingly in such cases.

Selection operations are a crucial aspect of query processing, and there are various algorithms and index structures available to streamline and optimize the selection process. From the straightforward linear search to the more complex primary and secondary index searches, each algorithm has its strengths and limitations, and their respective costs must be carefully considered in determining the most efficient approach.

### Sorting

Sorting data in database systems is a crucial task with multiple benefits. First, it enables SQL queries to specify the output to be sorted. Second, sorting helps enhance the efficiency of relational operations such as joins when the input relations are sorted. Therefore, sorting is a fundamental step that precedes the discussion of join operations.

![Figure 186 - Example](186.png)

While building an index on the sort key can sort a relation, it orders the relation logically through an index rather than physically. This process can lead to disk access for each record, making it very expensive. Hence, it may be preferable to sort records physically.

Sorting has been studied extensively for relations that are bigger than memory. The most commonly used technique for external sorting is the external sort–merge algorithm. This technique involves creating sorted runs with each run sorted but containing only some of the records of the relation. Then, the runs are merged, and the output is the sorted relation. The merge stage operates by reading one block of each file into a buffer block in memory and then choosing the first tuple (in sort order) among all buffer blocks. The output of the merge stage is a generalization of the two-way merge used by the standard in-memory sort–merge algorithm, but it merges N runs, so it is called an N-way merge.

![Figure 187 - External sorting using sort–merge](187.png)

If the relation is much larger than memory, there may be M or more runs generated in the first stage, and it is not possible to allocate a block for each run during the merge stage. In this case, the merge operation proceeds in multiple passes. Each pass reduces the number of runs by a factor of M − 1, and the passes repeat as many times as required until the number of runs is less than M. Finally, a final pass generates the sorted output.

![Figure 188 - Formula](188.png)

The cost analysis of external sort–merge is calculated using the number of blocks containing records of relation r, with the total number of block transfers for external sorting of the relation being given by a specific formula. By understanding the sorting of data and the external sort–merge algorithm, one can enhance the efficiency of database systems and facilitate more efficient querying and sorting of data.

![Figure 189 - Formula](189.png)

### Join Operation

Join operations are a fundamental task in database management systems, allowing us to combine information from different relations based on some common attributes. In this regard, several algorithms have been proposed to efficiently compute the join of relations.

One of the most basic algorithms is the nested-loop join, which essentially consists of a pair of nested for loops. However, this algorithm is not very efficient, as it examines every pair of tuples in the two relations, resulting in a high computational cost.

To address this issue, the block nested-loop join algorithm was proposed, which processes the relations on a per-block basis rather than on a per-tuple basis. This variant pairs every block of the inner relation with every block of the outer relation and generates all possible pairs of tuples, satisfying the join condition.

![Figure 190 - Block nested-loop join](190.png)

The block nested-loop join algorithm provides a significant saving in block accesses, as each block in the inner relation is read only once for each block in the outer relation, instead of once for each tuple in the outer relation. Furthermore, the cost of this algorithm can be further optimized by using the smaller relation as the inner relation.

Overall, these algorithms enable us to perform efficient join operations on large-scale relational databases, providing a powerful tool for data analysis and decision-making.

The merge-join algorithm stands tall as a formidable tool for computing natural and equi-joins. Boasting a structure, not unlike the merge stage of the merge-sort algorithm, merge-join offers a quick and efficient means of joining two relations, r(R) and s(S), sorted on their shared attributes R ∩ S.

Central to the merge-join algorithm is the use of pointers that move through the relations as groups of tuples with identical values on the join attributes are read into sets Ss. If each set fits into the main memory, the algorithm proceeds apace; otherwise, the algorithm will perform a block nested-loop join, matching the larger sets with corresponding blocks of tuples in r with the same join attribute values.

![Figure 191 - Merge join](191.png)

Once the input relations have been sorted, tuples with identical join attribute values are in consecutive order, resulting in each tuple being read only once. Consequently, with just one pass through each file, the merge-join algorithm proves to be an economical choice. Assuming that multiple buffer blocks are allocated to each relation, the cost of disk seeks is kept relatively low compared to data transfer.

![Figure 192 - Sorted relations for merge join](192.png)

Despite its many advantages, merge-join does have its limitations. Should either of the input relations r and s not be sorted on the join attributes, sorting must be done before the algorithm can be used, adding to the overall cost of computation. Additionally, if some sets of Ss are too large to fit into memory, the algorithm's efficiency may take a hit.

![Figure 193 - Hash partitioning of relations](193.png)

All in all, the merge-join algorithm remains a powerful tool in the database management arsenal, capable of handling natural and equi-joins with ease, provided the relations are sorted and the memory is allocated correctly.

The hash-join algorithm is a powerful technique that facilitates the computation of natural joins of relations r and s. It operates by utilizing a hash function to determine if an r tuple and an s tuple satisfy the join condition. If their values for the join attributes are the same, the r tuple can be found in the partition corresponding to the hash value of the join attribute, while the s tuple can be found in the same partition of the s relation. This avoids the need to compare r tuples with s tuples in any other partition, thereby enhancing the efficiency of the join operation.

![Figure 194 - Hash join](194.png)

The hash-join algorithm involves building a hash index on each partition of the s relation in memory, and then probing it with tuples from the corresponding partition of the r relation. This process requires only a single pass through both inputs, making it highly efficient. However, if the number of partitions is greater than the number of available buffer blocks, recursive partitioning is required to split the input into smaller partitions.

Furthermore, the hash-table overflow may occur due to the hash index being larger than the main memory. In such cases, the fudge factor is used to increase the number of partitions and reduce the size of each partition to handle the skewness. Overall, the hash-join algorithm is a powerful tool for computing natural joins efficiently and effectively.

Complex joins present a unique challenge. While nested-loop and block nested-loop joins can be applied regardless of join conditions, the more efficient techniques are limited to simple conditions such as natural and equi-joins. However, there is a way to implement joins with complex conditions such as conjunctions and disjunctions by utilizing the techniques developed for handling complex selections.

![Figure 195 - Example](195.png)

To illustrate this point, let us consider a join with a conjunctive condition. By applying one of the simpler joins on the individual conditions, we can generate an intermediate result consisting of tuples from both tables. The final join can then be obtained by testing the remaining conditions on this intermediate result.

![Figure 196 - Example](196.png)

![Figure 197 - Example](197.png)

![Figure 198 - Example](198.png)

A disjunctive join can be computed similarly, as the union of the records in individual joins. With this technique, complex joins need not be an insurmountable challenge, but rather a task that can be effectively managed with the proper tools and strategies.

### Other Operations

Several fundamental operations play a pivotal role in querying data. Along with the classic selection and join operations, relational databases also offer a handful of other operations that enable users to manipulate their data in novel ways.

One such operation is the elimination of duplicate records. This operation can be efficiently performed through the use of sorting or hashing techniques. While sorting allows for duplicates to be detected and removed as adjacent copies, hashing partitions the relation and constructs an in-memory hash index that can be used to remove any existing duplicates.

Projection is another powerful operation that allows for the selection of certain attributes from a relation. When applied, projection can produce a relation with duplicate tuples, which can be efficiently removed using the techniques discussed above.

Set operations such as union, intersection, and the set difference can be implemented through sorting or hashing as well. When sorting is used, both input relations are sorted and scanned only once to produce the desired result. When hashing is used, the two input relations are partitioned by a common hash function, and the respective partitions are then processed based on the desired operation.

Finally, outer join operations, which were previously introduced in section 4.1.2, can be implemented through two different strategies. One strategy is to compute the corresponding join and add further tuples to the result to get the outer join result. The other strategy is to use the techniques discussed earlier to compute the left outer join of two input relations, r, and s.

These operations are critical to the functionality of a relational database system, and their efficient implementation is key to the performance of such systems.

### Evaluation of Expressions

In this piece, we delve into the intricacies of evaluating expressions in the field of database systems. After exploring individual relational operations, we turn our attention to expressions containing multiple operations and the most effective ways to evaluate them.

One approach to evaluating an expression is to execute one operation at a time, in a logical order, and store each intermediate result in a temporary relation for later use. However, this method is not without its drawbacks, particularly when dealing with large data sets that require the creation of sizable temporary relations that must be written to disk.

![Figure 199 - Pictorial representation of an expression](199.png)

A more efficient alternative is pipelining, whereby multiple operations are executed simultaneously and the results of each operation are passed directly to the next, without the need for storing intermediate results. This approach is particularly useful when dealing with queries that generate results that need to be displayed in real-time, allowing users to receive query results as they are generated.

However, while pipelining can be a more efficient evaluation method, it is not always feasible, and in some cases, materialization is the only viable option. In addition, it is important to consider the cost of each approach when evaluating expressions, which can differ depending on the specific operations involved.

![Figure 200 - Double-pipelined join algorithm](200.png)

To implement a pipeline, a single complex operation can be constructed that combines the operations involved in the pipeline. However, it is often more desirable to reuse the code for individual operations to create a pipeline.

The evaluation of expressions in database systems is a complex and multi-faceted process that requires careful consideration of the specific operations involved, as well as the most efficient evaluation methods available.

## Query Optimization

Query optimization is a critical task in the realm of database management, and it involves selecting the most efficient approach for processing complex queries. It is not expected that users will write their queries in a manner that is optimized for processing efficiency. Rather, the system is tasked with the responsibility of devising a query evaluation plan that minimizes the cost of query evaluation. This is where the intricate art of query optimization comes into play.

Optimization occurs at various levels, including the relational-algebra level, where the system endeavors to identify an expression that is equivalent to the given expression but more efficient to execute. Another level of optimization involves selecting a detailed strategy for processing the query, such as choosing the algorithm to use for executing an operation or determining the specific indices to use.

The difference in evaluation time between a good and a bad strategy can be staggering, often spanning several orders of magnitude. Therefore, it is worth investing a considerable amount of time in the selection of a suitable strategy for processing a query, even if it is executed only once. The importance of query optimization cannot be overstated, as it ultimately leads to enhanced performance and productivity in database management.

### Overview

In the complex world of database systems, query optimization is a key component of efficient data retrieval. The process involves generating alternative query-evaluation plans and selecting the least-costly one to produce the same result as the original expression. The query optimizer achieves this by applying logical equivalence rules to generate equivalent expressions and then annotating these expressions in alternative ways to generate various evaluation plans.

To estimate the cost of each plan, the optimizer leverages statistical information about the relations, such as relation sizes and index depths, and uses this data to estimate the costs of individual operations. These costs are combined to determine the estimated cost of evaluating a given relational algebra expression.

Moreover, materialized views are utilized to speed up the processing of certain queries. Maintaining these views and performing query optimization with them is a separate challenge altogether.

While the best way to view the evaluation plan for a given query is through the GUI provided by the database system, command line interfaces offer variations of a command that display the execution plan chosen for a specified query. These commands vary by database, but all display the estimated costs along with the plan.

In short, query optimization is a vital aspect of database systems that requires a deep understanding of equivalence rules, statistics, and materialized views. Through the use of evaluation plans and estimated costs, the query optimizer seeks to reduce the time and resources required for data retrieval and ensure optimal performance of the system.

### Transformation of Relational Expressions

As we delve deeper into the world of database querying, we find ourselves exploring the concept of relational expression transformation. This involves the consideration of alternative expressions that generate the same set of tuples as the original relational expression on every legal database instance, albeit with varying evaluation costs. Such alternative expressions are said to be equivalent.

Equivalence rules serve as a guide for the transformation of relational-algebra expressions into other logically equivalent expressions. These rules can be used to replace an expression of the first form with an expression of the second form or vice versa. As a result, the optimizer is better equipped to transform expressions into more optimized, efficient, and logically equivalent ones.

![Figure 230 - Multiple transformations](230.png)

Among the many general equivalence rules governing relational-algebra expressions, the conjunctive selection operation can be deconstructed into a sequence of individual selections, and selection operations are commutative. Furthermore, only the final operations in a sequence of projection operations are needed. Selections can be combined with Cartesian products and theta joins, which are commutative, associative, and important for join reordering in query optimization.

The selection operation distributes over the theta-join operation under certain conditions, and the projection operation distributes over the theta-join operation under other conditions. Set union and intersection are commutative and associative, while the set difference is not commutative. Additionally, the selection operation distributes over the union, intersection, and set-difference operations.

![Figure 241 - EProcedure to generate all equivalent expressionsxample](241.png)

As we embark on this journey of database querying and the transformation of relational expressions, let us remember that the end goal is not only to generate the same set of tuples but to do so efficiently, logically, and with precision.

### Estimating Statistics of Expression Results

In this section, we delve into the intricate details of estimating statistics for database relations. The aim is to provide a framework for estimating the cost of operations based on their input size and other pertinent information. Our focus lies in exploring the statistical information maintained in database catalogs, and how this information can be harnessed to provide cost estimates for a range of relational operations.

We begin by examining the statistical information stored in database catalogs, which includes the number of tuples and blocks in a relation, the size of a tuple, the blocking factor of a relation, and the number of distinct values that appear in a relation for a particular attribute. This last statistic is particularly useful, as it is the same as the size of the attribute's domain in the relation. We also note that statistics about indices, such as the height of B+-tree indices and the number of leaf pages in the indices, are also maintained in the catalog.

However, it is important to bear in mind that the estimates we derive from these statistics are not always precise, as they rely on certain assumptions that may not hold in reality. As a result, the lowest estimated execution cost may not necessarily equate to the lowest actual execution cost. Nevertheless, real-world experience has shown that the plans with the lowest estimated costs are often either the lowest actual execution costs or close to them.

To maintain accurate statistics, it is necessary to update them every time a relation is modified. However, updating the statistics incurs a significant amount of overhead, which is why most systems only update statistics during periods of light system load. Consequently, the statistics used to choose a query-processing strategy may not be completely accurate, although they are often sufficient to provide good estimates of the relative costs of different plans.

Furthermore, in addition to the simplified statistical information outlined above, real-world optimizers often maintain further statistical information, such as histograms of attribute distributions, to improve the accuracy of cost estimates for evaluation plans. These histograms divide the values for an attribute into a number of ranges, and for each range, associate the number of tuples whose attribute value falls within that range, as well as the number of distinct attribute values in that range.

This section highlights the importance of maintaining accurate statistical information in database catalogs to enable cost estimates for relational operations. The estimation process is not without its challenges, particularly due to the assumptions involved. Nevertheless, the use of statistical information is essential for achieving efficient query-processing strategies in real-world database systems.

We delve into the intricate details of estimating statistics for database relations. The aim is to provide a framework for estimating the cost of operations based on their input size and other pertinent information. Our focus lies in exploring the statistical information maintained in database catalogs, and how this information can be harnessed to provide cost estimates for a range of relational operations.

We begin by examining the statistical information stored in database catalogs, which includes the number of tuples and blocks in a relation, the size of a tuple, the blocking factor of a relation, and the number of distinct values that appear in a relation for a particular attribute. This last statistic is particularly useful, as it is the same as the size of the attribute's domain in the relation. We also note that statistics about indices, such as the height of B+-tree indices and the number of leaf pages in the indices, are also maintained in the catalog.

However, it is important to bear in mind that the estimates we derive from these statistics are not always precise, as they rely on certain assumptions that may not hold in reality. As a result, the lowest estimated execution cost may not necessarily equate to the lowest actual execution cost. Nevertheless, real-world experience has shown that the plans with the lowest estimated costs are often either the lowest actual execution costs or close to them.

To maintain accurate statistics, it is necessary to update them every time a relation is modified. However, updating the statistics incurs a significant amount of overhead, which is why most systems only update statistics during periods of light system load. Consequently, the statistics used to choose a query-processing strategy may not be completely accurate, although they are often sufficient to provide good estimates of the relative costs of different plans.

Furthermore, in addition to the simplified statistical information outlined above, real-world optimizers often maintain further statistical information, such as histograms of attribute distributions, to improve the accuracy of cost estimates for evaluation plans. These histograms divide the values for an attribute into a number of ranges, and for each range, associate the number of tuples whose attribute value falls within that range, as well as the number of distinct attribute values in that range.

The estimation process is not without its challenges, particularly due to the assumptions involved. Nevertheless, the use of statistical information is essential for achieving efficient query-processing strategies in real-world database systems.

### Choice of Evaluation Plans

In the world of database optimization, the choice of evaluation plans is crucial in determining the best algorithm for each operation and coordinating the execution of those operations. With statistics estimated by various techniques, cost-based optimizers explore the space of query-evaluation plans equivalent to a given query and choose the one with the least estimated cost. However, when dealing with complex queries, generating all equivalent plans may be too expensive, leading to the use of heuristics that reduce optimization costs, albeit at the risk of not finding the optimal plan.

In SQL queries involving joins of a few relations, the optimal join order selection problem arises. For instance, given a join query, the number of different query plans that are equivalent to the query can be quite large, with the number of join orders rising quickly as the number of relations increases. Yet, by using dynamic-programming algorithms, we can store the results of computations and reuse them, reducing execution time significantly.

![Figure 256 - Dynamic-programming algorithm for join order optimization](256.png)

Such a dynamic-programming algorithm for finding optimal join orders is recursive, applying selections on individual relations at the earliest possible point, and taking into account all join conditions that relate attributes from the two subexpressions. The algorithm works by checking if the best plan for computing the join of a given set of relations has already been computed, then recording the best way of accessing a relation (taking selections into account) or trying every way of dividing a set into two disjoint subsets, recursively finding the best plans for each of the two subsets and computing the cost of the overall plan by combining the two. The use of associative arrays to store the evaluation plans computed by the algorithm makes the entire process more efficient and less time-consuming.

The optimization of query evaluation plans can be a daunting and computationally intensive task. The cost-based optimization approach, while effective, can suffer from the drawback of excessive computational costs. To mitigate this issue, heuristic rules can be employed to reduce the cost of optimization. However, the use of such heuristics can lead to suboptimal query evaluation plans, which may be more costly than optimal plans.

To address this issue, a general-purpose cost-based optimizer based on equivalence rules has been proposed. This optimizer leverages the power of physical equivalence rules to generate all possible evaluation plans while utilizing cost estimation techniques to select the optimal plan. However, the efficiency of this approach depends on several factors, including space-efficient expression representation, dynamic programming with memoization, and techniques that avoid generating all possible equivalent plans.

Despite the strengths of this approach, it remains complex and computationally intensive. To address this issue, heuristic rules are commonly employed in optimization. These rules can help to reduce the cost of query evaluation plans by performing selection and projection operations early in the process. While effective in many cases, the use of heuristic rules can lead to suboptimal query evaluation plans, and further heuristics are often employed to optimize the optimization process.

![Figure 257 - Left-deep join trees](257.png)

While cost-based optimization and heuristic rules have proved effective in many cases, the pursuit of optimal query evaluation plans continues to be a fascinating and elusive challenge for researchers and practitioners alike.

Optimizing nested subqueries in SQL can be a tricky task. SQL treats nested subqueries as functions that take parameters and return either a single value or a set of values. These parameters are the variables from an outer-level query that are used in the nested subquery, and they are known as correlation variables. The goal is to find an efficient way to evaluate a query with nested subqueries, since correlated evaluation, which evaluates the subquery for each tuple in the outer-level query, can result in a large number of random disk I/O operations.

SQL optimizers try to transform nested subqueries into joins where possible. Join algorithms help avoid expensive random I/O, which makes them a more efficient option. However, if the transformation isn't possible, the optimizer keeps the subqueries as separate expressions, optimizes them separately, and then evaluates them through correlated evaluation.

Transforming a nested subquery into a join isn't always straightforward. In some cases, creating a temporary relation that contains the results of the nested query and joining it with the outer-level query is necessary. The process of replacing a nested query with a join (possibly with a temporary relation) is called decorrelation.

Optimizing complex nested subqueries is a difficult task. While many optimizers do a limited amount of decorrelation, it is best to avoid using complex nested subqueries where possible. We cannot be sure that the query optimizer will succeed in converting them to a form that can be evaluated efficiently.

### Materialized Views**

Materialized views are a boon to databases, allowing for improved performance in certain applications. Whereas traditional views only store the query defining the view, materialized views go a step further, computing and storing the contents of the view. While this constitutes redundant data, the cost savings from reading a materialized view as opposed to computing the view using its query definition can be significant.

For example, a view providing the total salary for each department may require reading every instructor tuple pertaining to a department and summing the salary amounts, which can be a time-consuming process. However, if the view definition of the total salary amount was materialized, the total salary amount could be found by looking up a single tuple in the materialized view.

However, maintaining materialized views presents a challenge. Whenever the data used in a view definition changes, the materialized view must be kept up-to-date, a task known as view maintenance. While manual code updates can be used to maintain materialized views, this approach is error-prone and can lead to inconsistencies.

A better option for maintaining materialized views is to define triggers on insert, deleting, and update of each relation in the view definition. These triggers can modify the contents of the materialized view to reflect changes in the underlying data. Incremental view maintenance, whereby only affected portions of a materialized view are modified, is another option that modern database systems support.

The changes (inserts and deletes) to a relation or expression that can cause a materialized view to becoming out-of-date are referred to as its differential. The incremental maintenance of materialized views can be achieved through simple operations. For instance, to update a materialized view based on a join operation, we simply need to add the tuples that have been inserted into the old contents of the view.

Materialized views can significantly improve database performance, but maintaining their consistency is a challenge. With the support of modern database systems, however, it is possible to perform incremental maintenance of materialized views through simple operations.
The incremental maintenance of materialized views is a topic of great importance. Similar to projection operations, aggregation operations in SQL utilize count, sum, avg, min, and max to compute information from materialized views. However, the process of updating these aggregates on insertion or deletion of tuples is not always straightforward.

In the case of the count, a materialized view v = AGcount(B)(r) is created to compute the count of attribute B after grouping r by attribute A. On insertion, the system looks for the group t. A in the materialized view; if it is not present, a new entry (t.A, 1) is added. If the group already exists, the count for the group is incremented. Conversely, on deletion, the count for the group is decremented, and if it becomes zero, the tuple for group t.A is removed from the materialized view.

Handling sum aggregates requires an extra count value to distinguish between a group sum of zero and the case where the last tuple in a group is deleted. Similarly, computing the average requires the maintenance of sum and count aggregates, which are used to compute the average as the sum divided by the count.

Materialized views also enable the optimization of query operations, either by rewriting queries to utilize the view or by replacing the view with its definition. The implementation of these techniques can provide significant performance gains for database systems.

### Advanced Topics in Query Optimization**

In the realm of database management systems, there exist a myriad of opportunities for optimizing queries beyond the rudimentary techniques we have thus far explored. Let us delve into a few of these advanced optimization strategies.

First, let us examine the optimization of top-K queries. Often, queries retrieve results sorted according to certain attributes and require only the top K results. In some instances, the bound K is explicitly specified, while in others, the query may not mention the limit, but the optimizer can be signaled to retrieve only the top K results. When K is small, a query plan that generates the entire set of results before sorting and selecting the top K is highly inefficient, discarding most of the intermediate results that it computes. Consequently, novel approaches to optimizing top-K queries have emerged. For instance, one strategy involves using pipelined plans that can generate the results in sorted order. Another technique involves estimating the highest value on the sorted attributes that will appear in the top-K output and introducing selection predicates to eliminate larger values. If too few or too many tuples are generated, the selection condition is modified, and the query re-executed.

Next, we consider the optimization of join minimization, which arises when queries are generated through views. Occasionally, more relations are joined than needed for the computation of the query, leading to unnecessary computational overheads. In such cases, dropping a relation from a join is a typical example of join minimization. This technique can be performed in various situations, resulting in improved query performance.

Another optimization strategy is updating queries, which are notorious for involving subqueries in the set and where clauses, which must be taken into account in optimizing the update. Where an updated tuple may be reinserted in the index ahead of the scan and seen again by the scan, causing erroneous updates. 

Lastly, we delve into multi-query optimization and shared scans, where a query optimizer can potentially exploit common subexpressions between different queries, evaluating them once and reusing them where required. Complex queries may have subexpressions repeated in different parts of the query, which can be similarly exploited, reducing query evaluation costs. Such optimization is known as multi-query optimization and can even outperform common subexpression elimination in certain cases. A judiciously chosen set of query evaluation plans for a batch of queries may provide greater sharing and a lower cost than that offered by choosing the lowest cost evaluation plan for each query.

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
