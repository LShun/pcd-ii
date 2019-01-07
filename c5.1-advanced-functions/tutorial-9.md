# Tutorial 9
- [Tutorial 9](#tutorial-9)
  - [Q1](#q1)
  - [Q2](#q2)
  - [Q3](#q3)
  - [Q4](#q4)
  - [Q5](#q5)
    - [(i)](#i)
    - [(ii)](#ii)

## Q1

| Individual Elements | Passing (differences) | Whole Array |
| ------------------- | --------------------- | ----------- |
| The variable itself | What is passed | A pointer to the first element of the array |

## Q2

Trace table:

Output:
24
31
14
(Note: `i` starts from `size - 1`)

## Q3

```c
void arrayAverage(int m[], int size, int *total, double *average)
{
    int i;
    for (i = 0; i < size; i++)
        *total += m[i];
    *average = (double) *total / size;
}

arrayAverage(arr, 20, &total, &average);
```

## Q4

```c
From main, before calling the function:
a=1 b=2
c[0] = 10
c[1] = 20
c[2] = 30

 From the function, after modifying the values:
a=-999 b=-999
c[0] = -9
c[1] = -9
c[2] = -9

 From main, after calling the function:
a=-999 b=2
```

## Q5

### (i)

Function:

```c
void displayTitleName(Employee emp)
{
    printf("%s %s", emp.empTitle, emp.empSurname);
}
```

Example of function call:

```c
displayTitleName(emp);
```

### (ii)

Function:

```c
int isDatuk(Employee emp)
{
    if (strcmp(emp.empTitle, "Datuk") == 0))
    {
        return 0;
    }
    else return 1;
}
```

Example of function call:

```c
status = isDatuk(emp);
```