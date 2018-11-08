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

## Q3
```c
double hypotenuse(double a, double b)
{
    double hypotenuse;

    hypotenuse = sqrt(a*a + b*b);

    return hypotenuse;
}
```
