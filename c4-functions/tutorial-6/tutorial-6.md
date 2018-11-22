# Tutorial 6
## Q1
Write a function named inchToCm to convert inches (the input parameter) into
centimeters and return the result (using return statement). (1 inch = 2.54
centimeters.)
*Assume that the inch is in integer
```c
double inchToCm(int inch)
{
    double cm;

    cm = inch * 2.54;

    return cm;
}
```

## Q2
```c
double converter(int h)
{
    //variables
    double acres;

    //convert the hectars to acres
    acres = h * 2.47;

    //return the acres
    return acres;
}
```

## Q3
```c
double hypotenuse(double a, double b)
{
    double hypotenuse;

    hypotenuse = sqrt(a*a + b*b);

    return hypotenuse;
}
```

## Q4
char gradeOf(int score)
{
    if      (score >= 80 && score <= 100)
        return 'A';
    else if (score >= 70 && score <= 79)
        return 'B';
    else if (score >= 50 && score <= 69)
        return 'C';
    else if (score >= 40 && score <= 49)
        return 'D';
    else if (score >= 0 && score <= 39)
        return 'F';
    else 
        return 'X';
}

## Q5
(i)
```c
void f1(int a, double x);
```
(ii)
```
a=1, x=2.000000
a=3, x=4.300000
```

## Q6
(a)
```c
double calEpf(int salary)
{
    double ePF;

    ePF = salary * 0.11;

    return ePF;
}
```
(b)
```c
printf("Enter your salary: ");
scanf("%d", &salary);
ePF = calEpf(salary);
printf("Your EPF charges are: %f", ePF);
```

## Q8
### (i)
int mainMenu(void)
{
    int choice;

    printf("       Mathematics        \n"
           "       ===========        \n"
           "1. Addition\n"
           "2. Subtraction\n"
           "3. Multiplication\n"
           "4. Exit\n\n"
           "Press a number to make your selection: ");
    scanf("%d", &choice);
    return choice;
} 
###  (ii)
void addition(void)
{
    int answer;
    printf("       Addition           \n"
           "       ========           \n\n"
           "13 + 25 = ?\n\n"
           "Key in your answer and press <Enter>\n");
    scanf("%d", &answer);

    if (answer == (13+25))
        printf("Your answer is correct.\n");
    else
        printf("Your answer is incorrect. \n");
}

### (iii)

int main(void)
{
    int choice;
    do
    {
        choice = mainMenu();
        switch(choice)
        {
            case 1:
                addition();
                break;
            case 2:
                subtraction();
                break;
            case 3:
                multiplication();
                break;
            case 4:
                exit(-1);
            default:
                printf("Invalid entry.\n");
        }
    }
    while (choice < 1 || choice > 4);
}