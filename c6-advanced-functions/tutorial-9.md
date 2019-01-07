# Tutorial 9
- [Tutorial 9](#tutorial-9)
  - [Q1](#q1)
  - [Q2](#q2)
  - [Q3](#q3)


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