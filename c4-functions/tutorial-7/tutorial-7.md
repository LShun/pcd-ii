# Tutorial 7
## Q1
### Explain the difference between pass by value and pass by address in parameter
passing.
```
Ans:
Pass by value gives a copy of the variable itself. Pass by address gives a copy
of the address pointing to the variable to the function.
```
Local variables passed by value will be destroyed after the function ends. Local
variables passed by address are not destroyed after the function ends.

## Q2
### Write a function prototype for a function named calculate that returns void and contains an integer value parameter x, and a reference parameter to a long double, y. 
Ans:
`void calculate(int x, long double* y);`

## Q3
### a
`void func1(int b, int c);`

### a(ii)
`a = 5, b = 2`

### b
int funct2(int p, int q, int *product)
{
    *product = p * q;

    return p-q;
}

