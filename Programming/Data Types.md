# Data Types

Data types define what kind of value a variable can hold

| Type                          | Example       | Meaning                                         |
| ----------------------------- | ------------- | ----------------------------------------------- |
| Integer                       | 8, 100, -25   | Whole numbers, both positive and negative       |
| Float (floating-point number) | 0.44, -12.34  | Numbers with fractional/decimal parts           |
| Character                     | 'x', 'A', '4' | Any character inside **single** quotes          |
| String                        | "abc", "A100" | One or more characters inside **double** quotes |

*For indentation: use tab key, **NOT** spacebar*

## Variables

A piece of memory set aside in a program to store data

| Type                          | Data Type | Example       | Meaning                                     |
| ----------------------------- | --------- | ------------- | ------------------------------------------- |
| Integer                       | `int`     | 8, 100, -25   | Whole numbers, both positive and negative   |
| Float (floating-point number) | `float`   | 0.44, -12.34  | Number with fractional/decimal parts        |
| Character                     | `char`    | 'x', 'A', '4' | Any character inside single quotes          |
| String                        | soon...   | "abc", "A100" | One or more characters inside double quotes |

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
	
	return 0;
}
```

`*.h` is a **header** file

Every C program must only have **ONE** `main()` function

## Assignment Operation

For assigning some data into a variable

```c
int number;
number = 10;
```

## Integer Data Types

| Type    | Size    | Range                          | Delimiter |
| ------- | ------- | ------------------------------ | --------- |
| `short` | 2 bytes | \[ -32,000 , 32,000 ]          | `%sd`     |
| `int`   | 4 bytes | \[ -2 billion , 2 billion ]    | `%d`      |
| `long`  | 8 bytes | \[ -Huge Number, Huge Number ] | `%ld`     |

## Float Data Types

| Type     | Size    | Range                          | Delimiter |
| -------- | ------- | ------------------------------ | --------- |
| `float`  | 4 bytes | \[ -2 billion, 2 billion ]     | `%f`      |
| `double` | 8 bytes | \[ -Huge Number, Huge Number ] | `%lf`     |

| Type        | Size   | Range                          | Delimiter |
| ----------- | ------ | ------------------------------ | --------- |
| `char`      | 1 byte | N/a                            | `%c`      |
| `bool(ean)` | 1 byte | `true` or `false` / `1` or `0` | `%b`      |

## Unsigned Variables

*takes the negative range of a numeric variable and place it in the positive range*

| Type             | Size    | Range               | Delimiter |
| ---------------- | ------- | ------------------- | --------- |
| `unsigned short` | 2 bytes | \[ 0, 64,000 ]      | `%usd`    |
| `unsigned int`   | 4 bytes | \[ 0 , 4 billion ]  | `%ud`     |
| `unsigned long`  | 8 bytes | \[ 0, Huge Number ] | `%uld`    |

## Rules for Naming Variables

A variable-

1. must be constructed with letters (a-z, A-Z), numerals (0-9), or an underscore (\_)
2. must start with a letter or underscore
3. must not be a reserved name for C (eg. `main`)
4. can contain any number of characters, but is advised to keep it as short as possible

eg.

- `month_1_sales` - Valid
- `month1sales` - Valid
- `1st_month_sales` - Invalid
- `char` - Invalid

## Casting

*temporarily changing a data type from one data type to another*

```c
int a = 5;
int b = 2;

float result = a / b; // prints 2.000000????
```

*when two integers are divided together, they **always** return an integer*

*to change this, we have to **cast** one of them to a float*

```c
int a = 5;
int b = 2;

float result = (float)a / b; // prints 2.500000
```

*remember, casting is **temporary**; variable goes back to normal after the line*

```c
int a = 5;
int b = 2

float c = (float)b; // b casted to float
int d = b; // b no longer casted to float
```

### Implicit vs Explicit Casting

*there exists two types of casting in the C language: **implicit** and **explicit***

#### Implicit

*performed automatically by the C compiler. it is also known as type promotion*

eg.

```c
int i = 10;
double d = i // Implicit casting from int to double

printf("int: %d, double %f\n", i, d);
```

#### Explicit

*manually converting a variable from one data type to another. it is done with the following syntax:* `(new_type) value`

eg.

```c
double d = 9.7;
int i = (int)d; // explicit casting from double to int;
```
