# Macros

- **Macros**

Macros (a.k.a. "symbolic names") are used to avoid hard-coding values in programs

They **cannot be changed**, meaning they have a *constant value* of whatever they were defined as

## Declaring macros

```c
#define MACRO_NAME data_value
```

e.g.

```c
#define SIZE 10
#define GOON 'd'
```

Macro names are conventionally styled in **all caps**

## Macros vs variables

You can use macros instead of variables, but there is one crucial difference between them

Macros are technically **just text**, i.e. whenever a macro is found in code, the compiler **replaces all instances of the macro's name with it's value**

e.g.

```c
#define SIZE 10

int array[SIZE];
```
