# DATABASE SYSTEM CONCEPTS

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

**SPECIALTY DATABASES**

*Object-Based Databases*

*XML*

**ADVANCED TOPICS**

*Advanced Application Development*

*Spatial and Temporal Data and Mobility*

*Advanced Transaction Processing*

# Introduction

### Database-System Applications 
### Purpose of Database Systems 
### View of Data 
### Database Languages
### Relational Databases 
### Database Design 
### Data Storage and Querying 
### Transaction Management 
### Database Architecture 
### Data Mining and Information Retrieval 
### Specialty Databases 
### Database Users and Administrators
### History of Database Systems 

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
