# Arithmetic Operations and Expressions

Expressions combine variables, operators, and values to produce a result

```c
int num1;
int num2;
int num3;

// assign 20 to num1
num1 = 20;

// copy contents of num1 into num3 and then into num2
num2 = num3 = num1;
```

## Operators

| Operator | Meaning                            |
| -------- | ---------------------------------- |
| `+`      | Addition                           |
| `-`      | Subtraction                        |
| `/`      | Division                           |
| `*`      | Multiplication                     |
| `%`      | Modulus (remainder after division) |

```c
int var1 = 2;
int var2 = 10;

var1 + var2; // 12
var2 - var1; // 8
var2 * var1; // 20
var2 / var1; // 5
var2 % var1; // 0
```

## Increment and Decrement

| Operator | Meaning                   |
| -------- | ------------------------- |
| `++`     | Increment (increase by 1) |
| `--`     | Decrement (decrease by 1) |
| `+=`     | Addition short-hand       |
| `-=`     | Subtraction short-hand    |
| `*=`     | Multiplication short-hand |
| `/=`     | Division short-hand       |

```c
int var1 = 1;
int var2 = 5;

var1++; // 2
var2--; // 4
```

## Operator Precedence

```c
int num1 = 0;
num1 = 4 + 6 / 2;
printf("num1 contains %d", num1); // prints 7
```

*Most languages like C have mathematical order of precedence*

1. **Braces** ()
2. **-** (Unary minus) eg. `int a = 10; int b = -a + 2 / 6`
3. **\* / %** eg. `int a = 10 / 5 + 2`

*When there are operators of the same precedence, C executes them from **left to right***
