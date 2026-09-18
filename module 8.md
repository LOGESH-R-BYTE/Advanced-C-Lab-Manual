## EXP NO:6

### C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER

## Aim:

To write a C program print the lowercase English word corresponding to the number.

## Algorithm:

1. Start.
2. Initialize an integer variable `n`.
3. Read the value of `n`.
4. Use a switch statement:

   * Case 1: Print `"seventy one"`
   * Case 2: Print `"seventy two"`
   * Case 3: Print `"seventy three"`
   * Case 4: Print `"seventy four"`
   * Case 5: Print `"seventy five"`
   * Case 6: Print `"seventy six"`
   * Case 7: Print `"seventy seven"`
   * Case 8: Print `"seventy eight"`
   * Case 9: Print `"seventy nine"`
   * Default: Print `"Greater than 9"`
5. Exit the program.

## Program:

```c
#include <stdio.h>

int main()
{
    int n;

    printf("Enter a number: ");
    scanf("%d", &n);

    switch(n)
    {
        case 1:
            printf("seventy one");
            break;

        case 2:
            printf("seventy two");
            break;

        case 3:
            printf("seventy three");
            break;

        case 4:
            printf("seventy four");
            break;

        case 5:
            printf("seventy five");
            break;

        case 6:
            printf("seventy six");
            break;

        case 7:
            printf("seventy seven");
            break;

        case 8:
            printf("seventy eight");
            break;

        case 9:
            printf("seventy nine");
            break;

        default:
            printf("Greater than 9");
    }

    return 0;
}
```

## Output:

Enter a number: 1
seventy one

## Result:

Thus, the program is verified successfully.

---

## EXP NO:7

### C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS IN A SINGLE LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3

## Aim:

To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.

## Algorithm:

1. Start.
2. Declare character array `a[50]`.
3. Declare integer variables `h`, `i`, and `c`.
4. Read the string from the user.
5. Use an outer loop for each digit from 0 to 3.
6. Initialize counter `c` to 0.
7. Check each character in the string.
8. If the character matches the current digit, increment `c`.
9. Print the count followed by a space.
10. Repeat for digits 0 to 3.
11. End.

## Program:

```c
#include <stdio.h>
#include <string.h>

int main()
{
    char a[50];
    int h, i, c;

    printf("Enter the string: ");
    scanf("%s", a);

    for(h = 0; h <= 3; h++)
    {
        c = 0;

        for(i = 0; i < strlen(a); i++)
        {
            if(a[i] == h + '0')
            {
                c++;
            }
        }

        printf("%d ", c);
    }

    return 0;
}
```

## Output:

Enter the string: 01230123
2 2 2 2

## Result:

Thus, the program is verified successfully.

---

## EXP NO:8

### C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER

## Aim:

To write a C program to print all of its permutations in strict lexicographical order.

## Algorithm:

1. Start.
2. Declare a character pointer `s`.
3. Dynamically allocate memory for the string.
4. Check whether memory allocation is successful.
5. Read the string from the user.
6. Call the `permute()` function to generate permutations.
7. Use the `swap()` function to exchange characters.
8. Print each generated permutation.
9. Free the allocated memory.
10. End.

## Program:

```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

void swap(char *x, char *y)
{
    char temp;
    temp = *x;
    *x = *y;
    *y = temp;
}

void permute(char *str, int l, int r)
{
    int i;

    if(l == r)
    {
        printf("%s\n", str);
    }
    else
    {
        for(i = l; i <= r; i++)
        {
            swap((str + l), (str + i));
            permute(str, l + 1, r);
            swap((str + l), (str + i));
        }
    }
}

int main()
{
    char *s;

    s = (char *)malloc(100 * sizeof(char));

    if(s == NULL)
    {
        printf("Memory allocation failed");
        return 1;
    }

    printf("Enter a string: ");
    scanf("%s", s);

    printf("Permutations are:\n");

    permute(s, 0, strlen(s) - 1);

    free(s);

    return 0;
}
```

## Output:

Enter a string: ABC
Permutations are:
ABC
ACB
BAC
BCA
CBA
CAB

## Result:

Thus, the program is verified successfully.

---

## EXP NO:9

### C PROGRAM TO PRINT A PATTERN OF NUMBERS FROM 1 TO N AS SHOWN BELOW

## Aim:

To write a C program to print a pattern of numbers from 1 to `n` as shown below.

## Algorithm:

1. Start.
2. Declare integer variables `n`, `i`, `j`, `min`, and `len`.
3. Read the value of `n` from the user.
4. Calculate the length of the square matrix using `len = n * 2 - 1`.
5. Use nested loops to generate the matrix.
6. Calculate the minimum distance from the current position to the borders.
7. Print `n - min`.
8. Repeat for all rows and columns.
9. End.

## Program:

```c
#include <stdio.h>

int main()
{
    int n, i, j, min, len;

    printf("Enter the value of n: ");
    scanf("%d", &n);

    len = n * 2 - 1;

    for(i = 0; i < len; i++)
    {
        for(j = 0; j < len; j++)
        {
            min = i;

            if(j < min)
                min = j;

            if(len - 1 - i < min)
                min = len - 1 - i;

            if(len - 1 - j < min)
                min = len - 1 - j;

            printf("%d ", n - min);
        }

        printf("\n");
    }

    return 0;
}
```

## Output:

Enter the value of n: 3

```text
3 3 3 3 3
3 2 2 2 3
3 2 1 2 3
3 2 2 2 3
3 3 3 3 3
```

## Result:

Thus, the program is verified successfully.

---

## EXP NO:10

### C PROGRAM TO FIND A SQUARE OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

## Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

## Algorithm:

1. Start.
2. Define a function `square()` with no parameters.
3. Declare an integer variable inside the function.
4. Get the number from the user.
5. Calculate the square by multiplying the number by itself.
6. Return the squared value.
7. In the `main()` function, call the `square()` function.
8. Display the result.
9. End.

## Program:

```c
#include <stdio.h>

int square()
{
    int n;

    printf("Enter a number: ");
    scanf("%d", &n);

    return n * n;
}

int main()
{
    int result;

    result = square();

    printf("Square = %d", result);

    return 0;
}
```

## Output:

Enter a number: 5
Square = 25

## Result:

Thus, the program is verified successfully.
