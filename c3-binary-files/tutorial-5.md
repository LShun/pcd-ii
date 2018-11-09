# Tutorial 5
## Q1

| Text File | Differences | Binary Files |
| --------- | ----------- | ------------ |
| Text data | Type of data stored | Binary data, in memory format. |
| Readable | Human Readability | Not readable |
| Lines present. Each line is ended by a '\n' character. | Lines | No lines or newline character. |

##  Q3
```c
fPtr = fopen("binary.bin", "wb");
```

```c
fwrite(fPtr, sizeof(char), 10, str);
```

