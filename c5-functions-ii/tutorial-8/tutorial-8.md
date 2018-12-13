# Tutorial 8
- [Tutorial 8](#tutorial-8)
  - [1.](#1)
  - [2.](#2)
  - [3.](#3)
    - [a)](#a)
    - [b)](#b)
    - [c)](#c)
  - [Q4](#q4)
    - [a](#a)
- [5.](#5)
  - [(a)](#a)
  - [(b)](#b)
- [6.](#6)
  - [(a)](#a-1)
  - [(b)](#b-1)

## 1.
- `auto`
    - The default type for formal parameters and local variables
    - Automatically allocated and deallocated on stack when function is called
      and returns.
- `static`
    - Space for static local variables are allocated and initialized once,
      conceptually at
      compile time
    - Persistent, not destroyed when function terminates.
    - Remain allocated until program terminates
- `register`
    - Suggests the compiler to try storing the variable in the register to speed
    up access time
    - Does not have a memory location. Cannot be passed by address as a parameter.
- `extern`
    - Any variable defined outside function is `extern` by default.
    - Available without declaration to any function appearing after definition
      in same source file.
    - Also known as global variable.
    - Does not allocate memory, simply provides type information to compiler.
## 2.
```
The purpose of the `register` keyword is to suggest to the compiler to place the variable in the register of the CPU. This is to speed up access time and reduce bytecode size at the cost of referencing by address causes undefined behavior.
```

## 3. 
### a)
| Local variable | Global Variable |
| -------------- | --------------- |
| Destroyed when function ends | Destroyed when program terminates |

### b)
`static`

### c)
A variable can be made accessible by declaring it as a global variable or an
`extern` variable. The variable has the scope of the whole source file,
therefore is not deallocated when any function returns. The inherent danger is
that unwanted modifications can be done to the global variable because it exists
throughout the entire program, and can be hard or near impossible to trace in
large programs.

## Q4
### a
| Variable | Visibility | Storage Class |
| -------- | ---------- | ------------- |
| x at line 6 | Entire program | `extern` |
| z at line 23 | In fun2() | `auto` |

(b)
```

2   
4   
12   
48
4
```
# 5.
## (a)
A = extern
B = auto
C = auto
D = static
E = auto

## (b)
22
22
23
43
24
65

# 6.
## (a)
| Variable Name | Line Number | Storage Class | Scope (Line Num) |
| ------------- | ----------- | ------------- | ---------------- |
| x | 3 | `extern` | 3-26 |
| c | 7 | `auto` | 7-10 |
| y | 12 | `static` | 12-26 |
| x | 16 | `auto` | 16-18 |
| d | 20 | `extern` | 20-26 |
| w | 22 | `auto` | 22-26 |
| v | 24 | `static` | 24-26 |

## (b)
1. `register` variables cannot be referenced/dereferenced. This is because they
   are stored in the CPU registers, which does not have memory location
   associated.
2. Register storage size is extremely limited. Therefore, in default, the
   compiler will automatically allocate variables into registers in the best way
   possible. Using `register` keyword suboptimally can lead to degraded performance.


