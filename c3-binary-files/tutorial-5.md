# Tutorial 5
## Q1

| Text File | Differences | Binary Files |
| --------- | ----------- | ------------ |
| Text data | Type of data stored | Binary data, in memory format. |
| Readable | Human Readability | Not readable |
| Lines present. Each line is ended by a '\n' character. | Lines | No lines or newline character. |

##  Q2

`Coord point = {'7', '8'}` -> `Coord point = {7, 8}`
The `point` variable is initialized with the ASCII representation of 7 and 8,
not the actual number of 7 and 8.

`fread(point, sizeof(Coord), 1, sp);` -> `fwrite(point, sizeof(Coord), 1, sp);`
The program needs to write to a file, not read from a file

`fclose("COORD.bin");` -> `fclose(sp);`
`fclose` closes a file pointer, not a file.

##  Q3
```c
fPtr = fopen("binary.bin", "wb");
```

```c
fwrite(fPtr, sizeof(char), 10, str);
```

## Q4
```c
#include <stdio.h>
#include <stdlib.h>

int main(void)
{
    //variables
    FILE *fIn, *fOut1, *fOut2;
    int number;

    fIn = fopen("integer.dat", "rb");
    fOut1 = fopen("odd.dat", "wb");
    fOut2 = fopen("even.dat", "wb");

    while(fread(&number, sizeof(int), 1, fIn) != EOF)
    {
        if(number%2 == 0)
            fwrite(&number, sizeof(int), 1, fOut2);
        else
            fwrite(&number, sizeof(int), 1, fOut1);
    }

    fclose(fIn);
    fclose(fOut1);
    fclose(fOut2);

    printf("Completed");
}
```
## Q5
```
while(fread(&p, sizeof(Product), 1, prodP) != EOF)
{
    profit = p.sellPrice - p.costPrice;
    printf("Enter unit sold: ");
    scanf("%d", &unit);
    s.prod = p;
    s.profit = profit;
    s.unitsSold = unit;
    fwrite(&s, sizeof(Sales), 1, salesP);
}