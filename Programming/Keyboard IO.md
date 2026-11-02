# Keyboard Input/Output

## Input

*useful for getting input from the user*

To get keyboard input from the user, we use the `scanf()` function. It reads input from the user.

You **must** place a `&` before the variable name in a `scanf()` statement. The character is used to pass the address of a variable to the function. `scanf()` requires a memory address of a variable to pass data into.

eg.

```c
int age;

printf("please enter age: \n");
scanf("%d", &age); // remember the `&` before the vai

printf("you are %d years old\n", age);
```

Alternatively we can use `getchar()`, which is only used to read a single character.

## Output

The screen is technically called **Standard Output**

To output to Standard Output, C uses the `printf()` statement:

```c
printf(".....");
```

A **Delimiter** displays the contents of a variable, represented by `%` followed by a character:

| Delimiter | Type                     |
| --------- | ------------------------ |
| `%d`      | Displays an integer      |
| `%f`      | Displays a float         |
| `%c`      | Displays a character     |
| `%%`      | Displays a '%' character |

## Escape Character

*Represented by a* `\`

It has multiple different functions:

| Character | Function                            |
| --------- | ----------------------------------- |
| `\n`      | Print a new line to standard output |
| `\t`      | Displays a tab to standard output   |

```c
#include <stdio.h>

int main()
{
	int var1;
	float var2;
	char var3;
	
	var1 = 10;
	var2 = 8.21;
	var3 = 'q';
	
	printf("var1 contains %d\nvar2contains %f\nvar3 contains %c", var1, var2, var3);
	
	return 0;
}
```
