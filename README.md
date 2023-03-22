# DATABASE SYSTEM CONCEPTS
The landscape of computer science education has undergone a profound transformation in recent years, as database management has emerged as a critical pillar in modern computing environments. To equip students with the essential knowledge about database systems, we present a comprehensive exploration of the fundamental concepts of database management, ranging from database design to database languages to database-system implementation.

Intended for students at the junior or senior undergraduate or first-year graduate level, this text provides both basic materials for an introductory course as well as advanced material suitable for supplemental or advanced study. Assuming only a familiarity with basic data structures, computer organization, and high-level programming languages like Java, C, or Pascal, we present concepts as intuitive descriptions, grounded in the running example of a university.

While important theoretical results are covered, we eschew formal proofs in favor of figures and examples that vividly illustrate the truth of a given result. Formal descriptions and proofs can be found in advanced texts and research papers referenced in the bibliographical notes.

This text is an indispensable resource for anyone seeking to acquire a deep understanding of database management, rooted in theoretical foundations but connected to practical applications.

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

### Overview of the SQL Query Language 
### SQL Data Deﬁnition 
### Basic Structure of SQL Queries 
### Additional Basic Operations 
### Set Operations 
### Null Values 
### Aggregate Functions 
### Nested Subqueries 
### Modiﬁcation of the Database 

## Intermediate SQL

### Join Expressions
### Views
### Transactions
### Integrity Constraints
### SQL Data Types and Schemas
### Authorization

## Advanced SQL

### Accessing SQL From a Programming Language
### Functions and Procedures
### Triggers 
### Recursive Queries** 
### Advanced Aggregation Features** 
### OLAP**

## Formal Relational Query Languages

### The Relational Algebra 
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
