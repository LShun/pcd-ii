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