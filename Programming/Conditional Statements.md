# Conditional Statements

In C and other languages, we can make choices in terms of code execution

## Operators

| Operator | Meaning                  |
| -------- | ------------------------ |
| `==`     | Equivalent to / Equal to |
| `!=`     | NOT equal to             |
| `<`      | Less than                |
| `>`      | Greater than             |
| `<=`     | Less than OR equal to    |
| `>=`     | Greater than OR equal to |
| `&&`     | AND                      |
| `\|\|`   | OR                       |
| `!`      | NOT (invert)             |

## Logical Statements

```c
float bank_balance = 0;

print("Enter bank balance: ");
scanf("%f", &bank_balance);

// `&&` ensures both conditions must be true to return true
if (bank_balance > 0 && bank_balance <= 100)
{
	printf("Your balance is between 1 and 100");
}

// `&&` ensures either conditions can be true to return true
if (bank_balance > 0 || bank_balance <= 100)
{
	printf("Your balance is between 1 and 100");
}
```

## If Statement

```c
if (condition)
{
	statement1;
	...
	statementN;
}
```

Condition **must** be true for code to run inside curly braces to execute; if false, it is ignored

eg.

```c
float bank_balance = 0;

// check if bank balance is greater than zero
int (bank_balance > 0)
{
	printf("You have money");
}
```

## If ... Else Statement

```c
if (condition)
{
	statement1;
	...
	statementN;
}
else
{
	statement1;
	...
	statementN;
}
```

If the condition is true, code after first set of `{}` is executed; if it's false, code inside the `{}`

***Note**: Always use curly the curly braces* (`{}`) *when using conditional statements*

## Nested If Statements

**Nested** statements are statements inside of other statements

```c
if (bank_balance > 0) // outer if
{
	if (bank_balance <= 100) // inner if
	{
		printf("\nYour balance is between 1 and 100");
	}
}
```

Try not to have more than **three layers of nesting**; it makes it harder to read and redesign the program

## Switch Statement

**Switch** statements are alternatives to multiple if else statements

```c
char grade = ' ';

printf("Enter a grade\n");
scanf("%c", &grade);

switch(grade)
{
	case 'A': // if (oper == 'A')
	{
		// code
		break; // break out of switch
	}
	case 'B':
	case 'b': // if (oper == 'B' || oper == 'b')
	{
		// code
		break;
	}
	default: // else
	{
		printf("Not a grade");
	}
}
```

They **only work with character and whole number variables**

## Terminology

- **Refactoring** - changing code without changing its meaning
- **Overhead** - running processing-intensive programs ( a lot of else ifs )
