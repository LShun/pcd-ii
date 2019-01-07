# T10 - Program Design

- [T10 - Program Design](#t10---program-design)
  - [Q1](#q1)
  - [Q2](#q2)
  - [Q3](#q3)
    - [(i) Pathological coupling](#i-pathological-coupling)
    - [(ii) Simple data coupling](#ii-simple-data-coupling)
    - [(iii) Coincidental cohesion](#iii-coincidental-cohesion)

## Q1

Levels of cohesion in program design.

- Most desirable: Function cohesion
- Sequential cohesion
- Communicational cohesion
- Procedural cohesion
- Logical cohesion
- Temporal cohesion
- Least desirable: Coincidental cohesion

## Q2

6 types of cohesion.

- Function cohesion
  - Function performs 1 task
  - Example: Compute cosine of angle
- Sequential cohesion
  - Function performs more than 1 task, all the tasks are related through data, and sequence is important
  - Example: Module format and cross validation of record
    - Use raw record
    - Format raw record
    - Cross-validate fields in raw record
    - Return formatted cross-validated record
- Communicational cohesion
  - Same as sequential cohesion, but sequence is not important.
  - Example: Determine customer details
- Procedural cohesion
  - Function perfors more than 1 task, all tasks are related by logic, and sequence is important
  - Example: Write, read, and edit something
- Logical cohesion
  - Same as procedural cohesion, but sequence is not important
  - Example: Display record in staff depending on the record type

## Q3

### (i) Pathological coupling

A type of coupling where a function modify other function's data.

### (ii) Simple data coupling

A type of coupling where function share data by passing parameters, and returning results.

### (iii) Coincidental cohesion

A type of cohesion in functions where the function performs more than 1 task which are completely unrelated to each other. The tasks just happens to be in a same function.