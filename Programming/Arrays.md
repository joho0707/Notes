# Arrays

In programming, sometimes you'll need many variables of the same type.

- **Array** - a collection of variables *of the same type*
- **Element** - an item inside of an array

An array is what is known as a **Data Structure**

Arrays are **contiguous**, meaning it is one single block of memory, i.e. it can't be split up across different locations of memory

## Declaring arrays

```c
array_data_t array_name[array_size_n];
```

Arrays must have *square brackets* `[]` after the variable name to be declared as an array

eg.

```c
int ages[5]; // array of 5 integers
float number_set[10]; // array of 10 floats
char name[12]; // array of 12 characters
```

Arrays use the *same amount of memory* as would declaring each element individually

eg.

```c
int a, b, c, d, e; // 20 bytes
int nums[5]; // 20 bytes
```

There is *no limit* to the amount of elements in an array. It only depends on the amount of RAM available.

An array **must know it's size before it's compiled**. Use dynamically-allocated memory array's instead.

## Arrays in memory

- **Index** - the first element of an array, or the location of any element

The index of an array is **always element 0**. The last element of the array is **1 minus the size the array size**, i.e. array of size 5; last element is at index 4

## Assigning elements

You can declare elements in an array as follows:

```c
int ages[10]; // array of 10 ages

ages[0] = 7;
ages[1] = 18;
ages[2] = 22;
...
```

The assignment operation `=` allows us to assign a value to an index in an array. You must include the brackets and the respective index, or it won't compile

### Using loops

Assigning individual elements in arrays is annoying, especially when using `scanf()`. You can use a loop instead:

```c
int ages[10];
int sum = 0;

for (i = 0; i < 10; i++)
{
    // using `i` to find current index, enter input into `i`
    scanf("%d", &ages[i]);

    sum += ages[i];
}
```

## Initialising arrays

When you declare an array, the OS finds a uniform block of memory, dividing it by the length of the array. The data however, is completely random data until you declare each element individually.

To initialise an array, you do the following:

```c
array_data_t array[array_size_n] = { element_1, element2, ... , element_n }
```

You **must** use the curly braces `{}` to initialise each element.

eg.

```c
#define MONTHS_N 12

int days[MONTHS_N] = {31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31};

for (int i = 0; i < MONTHS_N; i++)
{
    printf("%d ", days[i]);
}
```

## Multi-dimentional arrays

2D arrays have two sets of square brackets `[]`

```c
type_t array_name [ rows_n ][ columns_n ];
```

They allow you to store **two or more sets of data** in one

## Initialising Mutli-dimentional arrays

```c
type_t array_name[ rows_n ][ colums_n ] = { (element_1, element_2), ... };
```

You can visualise multi-D arrays easier as such:

```c
// regular way
int array_1[4][3] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12};

// easier-to-read way
int array_2[4][3] = {   1, 2, 3,
                        4, 5, 6,
                        7, 8, 9,
                        10, 11, 12
                    };

// even-easier-to-read way
int array_3[4][3] = {   {1, 2, 3},
                        {4, 5, 6},
                        {7, 8, 9},
                        {10, 11, 12}
                    };
```

It's better to display multi-D arrays like this as it helps readers visualise how the array will look like in memory
