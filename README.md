# DATABASE SYSTEM CONCEPTS
The manual discusses the evolution of database management from a specialized computer application to an essential component of modern computing. It explains the fundamental concepts of database management, including database design, database languages, and database-system implementation, and is intended for a first course in databases at the junior or senior undergraduate, or first-year graduate, level. The manual assumes only a familiarity with basic data structures, computer organization, and a high-level programming language such as Java, C, or Pascal. The authors present concepts as intuitive descriptions, with many based on a running example of a university. The manual covers important theoretical results but omits formal proofs, using figures and examples to suggest why a result is true. The concepts and algorithms presented are often based on those used in existing commercial or experimental database systems, but are presented in a general setting not tied to any one particular database system. The manual includes case studies in Part 9 and has been updated to reflect changes in the way databases are designed, managed, and used. It also takes into account trends in the teaching of database concepts and makes adaptations where appropriate.

The first chapter offers an introduction to database systems and an example application. Parts 1 and 2 cover relational databases and database design, respectively, with an emphasis on SQL and the entity-relationship data model. Part 3 focuses on data storage and querying, including storage devices, data structures, and query evaluation algorithms. Part 4 discusses transaction management, including atomicity, consistency, isolation, and durability, and covers techniques for ensuring serializability and correct transaction execution. Part 5 covers system architecture, including centralized systems, client-server systems, parallel and distributed architectures, and distributed databases. Part 6 introduces data warehousing, data mining, and information retrieval techniques. Part 7 covers specialty databases, including object-based databases and XML. Finally, Part 8 covers advanced topics, including spatial and temporal databases, and covers new trends such as NoSQL and NewSQL. The five appendices cover mathematical preliminaries, relational algebra, additional SQL, the Web and DBMSs, and advanced application development. The book is aimed at students, professionals, and researchers interested in learning about the concepts and principles of database systems.

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

## Introduction to the Relational Model

### Structure of Relational Databases
### Database Schema
### Keys
### Schema Diagrams
### Relational Query Languages
### Relational Operations

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
