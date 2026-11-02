# Loops

Loops are blocks of code that repeat until a condition is met
In C, there exist 3 types of loops

## While loops

```c
int i = 0;

while (i < 10)
{
    printf("%d\n", i);
}

```

`while` loops are used to repeat code while a certain condition is true, and does not guarantee that the code inside is ran

## Do ... While loops

```c
int i = 0;

do
{
    printf("%d\n", i);
}
while (i < 10);
```

`do {} while` loops are similar to regular `while` loops, however they guarantee that the code inside the block is ran at least once

## For loops

```c
for (int i = 0; i <= 10; i++)
{
    printf("%d\n", i);
}
```

`for` loops are used to iterate over an **index** variable, they are arguably the most used loops in C
