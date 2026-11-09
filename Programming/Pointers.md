# Pointers

Every variable and data structure is stored in a unique memory address in RAM

```c
/*
    Program to display the memory address of a variable
*/

#include <stdio.h>

int main()
{
    int var1;
    char var2;

    var1 = 1;
    var2 = 'A';

    print("var1: %d, stored at: %p\n", var1, &var1);
    print("var2: %d, stored at: %p\n", var2, &var2);

    return 0;
}
```

Addresses in RAM are represented by a **hexadecimal number** i.e. 0x203718DF28301EA4. Use `%p` to display a pointer

## Pointer Variables

You can create a variable to point to the address of another variable:

```c
type_t *pointer;
```

Note the `*` before the variable name. Pointers **only store one thing: the address of another variable**.

```c
int number = 23; // creates a new int variable with data 23

int *p = &number; // creates a new pointer variable that points to the address of `number`
```
