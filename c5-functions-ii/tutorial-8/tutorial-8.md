# Tutorial 8

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

## 3. a)
| Local variable | Global Variable |
| -------------- | --------------- |
| Destroyed when function ends | Destroyed when program terminates |

## b)
`static`

## c)
A variable can be made accessible by declaring it as a global variable or an
`extern` variable. The variable has the scope of the whole source file,
therefore is not deallocated when any function returns. The inherent danger is
that unwanted modifications can be done to the global variable because it exists
throughout the entire program, and can be hard or near impossible to trace in
large programs.

