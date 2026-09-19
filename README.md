# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M5
# IAPR-5- Module 5 - FoC
## 9. Implementation of recursion.
## 10. Implementation of programs using pointer arithmetic.
# Ex.No:21
  Implement a C program to demonstrate call by value and call by reference by swapping two integers using separate functions.
# Date : 19/9/2026
# Aim:
 To implement a C program that illustrates the difference between call by value and call by reference by swapping two integer variables using two separate functions.
# Algorithm:
### Step 1:
  Start
### Step 2: 
  Include the standard input-output library: #include<stdio.h>.
### Step 3:
  Declare two functions:
  - `swapv(int, int)` for swapping using call by value  
  - `swapr(int *, int *)` for swapping using call by reference
### Step 4: 
  In the `main()` function, declare two integer variables `a` and `b` and initialize them with values (e.g., 10 and 20).
### Step 5: 
  Print the values of `a` and `b` before calling `swapv()`.
### Step 6: 
  Call the function `swapv(a, b)` and print the values of `a` and `b` after the function call to show that call by value does not change the original values.
### Step 7: 
  Print the values of `a` and `b` before calling `swapr()`.
### Step 8: 
  Call the function `swapr(&a, &b)` using the addresses of `a` and `b`.
### Step 9: 
  Print the values of `a` and `b` after the `swapr()` function call to show that call by reference successfully swaps the original values.
### Step 10: 
  Inside `swapv(x, y)` function:
  - **Step 10.1:** Swap the values of `x` and `y` using a temporary variable.  
  - **Step 10.2:** Print the swapped values (formal parameters).
### Step 11: 
  Inside `swapr(*x, *y)` function:
  - **Step 11.1:** Swap the values pointed to by `x` and `y`.  
  - **Step 11.2:** Print the swapped values (affects actual parameters).
### Step 12: 
  Stop
# Program:
#include <stdio.h>

// Function prototype
void validateDate();

int main()
{
    // Step 3: Call the function to validate date
    validateDate();
    return 0;
}

// Function definition
void validateDate()
{
    int dd, mm, yy;
    int isValid = 0; // Flag to check validity

    // Step 5 & 6: Input date
    printf("Enter date (DD/MM/YYYY): ");
    scanf("%d/%d/%d", &dd, &mm, &yy);

    // Step 7: Validate year
    if (yy < 1900 || yy > 9999)
    {
        printf("Year is not valid.\n");
        return;
    }

    // Step 8: Validate month
    if (mm < 1 || mm > 12)
    {
        printf("Month is not valid.\n");
        return;
    }

    // Step 9,10,11: Validate day based on month and leap year
    switch (mm)
    {
        case 1: case 3: case 5: case 7: case 8: case 10: case 12:
            if (dd >= 1 && dd <= 31)
                isValid = 1;
            break;
        case 4: case 6: case 9: case 11:
            if (dd >= 1 && dd <= 30)
                isValid = 1;
            break;
        case 2:
            // Leap year check
            if ((yy % 4 == 0 && yy % 100 != 0) || (yy % 400 == 0))
            {
                if (dd >= 1 && dd <= 29)
                    isValid = 1;
            }
            else
            {
                if (dd >= 1 && dd <= 28)
                    isValid = 1;
            }
            break;
    }

    // Step 12 & 13: Display result
    if (isValid)
        printf("Date is valid.\n");
    else
        printf("Date is invalid.\n");
}

# Output:
<img width="399" height="253" alt="image" src="https://github.com/user-attachments/assets/dd6e3d50-5b88-4979-9a79-bd0adb5c6df4" />

# Result: 
  Thus, the program was implemented and executed successfully, and the required output was obtained.


# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M5
# IAPR-5- Module 5 - FoC
# Ex.No:22
  Implement a C program to generate the Fibonacci series using a recursive function. The program should accept a positive integer n and display the first n terms of the Fibonacci sequence.
# Date : 19/9/2026
# Aim:
  To implement a C program that uses a recursive function to generate and display the Fibonacci series for a given number of terms.
# Algorithm:
### Step 1:
  Start
### Step 2: 
  Include the standard input-output library: #include<stdio.h>.
### Step 3:
  Declare a recursive function `fibo(int x)` that returns the Fibonacci number at position `x`.  
### Step 4:
  In the `main()` function, declare variables `n` and `i`.  
### Step 5:
  Prompt the user to enter a positive integer `n`.  
### Step 6:
  Read the value of `n`.  
### Step 7:
  Display a message indicating that the Fibonacci series of `n` terms will be printed.  
### Step 8:
  Use a `for` loop from `i = 0` to `i < n` to:  
  - **Step 8.1:** Call the recursive function `fibo(i)`  
  - **Step 8.2:** Print the returned Fibonacci value  
### Step 9:
 Define the recursive function `fibo(x)` as follows:  
 - **Step 9.1:** If `x == 0` or `x == 1`, return `x`.  
 - **Step 9.2:** Otherwise, return `fibo(x - 1) + fibo(x - 2)`.  
### Step 10:
  Stop
# Program:
# Output:
# Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.


# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M5
# IAPR-5- Module 5 - FoC
# Ex.No:23
   Implement a C program to demonstrate recursion by printing a sequence of even or odd numbers from a given lower limit to an upper limit, with each recursive call progressing by 2.
# Date : 
# Aim:
  To implement a C program that uses a recursive function to print even or odd numbers in a specified range based on the starting value provided by the user.
# Algorithm:
### Step 1:
  Start
### Step 2: 
  Include the standard input-output library: #include<stdio.h>. 
### Step 3:
  Declare a recursive function `printEvenOdd(int cur, int limit)` to print numbers from `cur` to `limit` with a step of 2.
### Step 4:
  In the `main()` function, declare two integer variables: `lowerLimit` and `upperLimit`.
### Step 5:
  Prompt the user to enter the lower limit of the range.
### Step 6:
  Read and store the lower limit.
### Step 7:
  Prompt the user to enter the upper limit of the range.
### Step 8:
  Read and store the upper limit.
### Step 9:
  Display a message indicating that the even/odd numbers in the given range will be printed.
### Step 10:
  Call the recursive function `printEvenOdd(lowerLimit, upperLimit)`.
### Step 11:
  Inside the function `printEvenOdd(cur, limit)`:
  - **Step 11.1:** If `cur > limit`, terminate the recursion.  
  - **Step 11.2:** If `cur == limit`, print the value without a trailing comma.  
  - **Step 11.3:** Otherwise, print the current value followed by a comma.  
  - **Step 11.4:** Recursively call `printEvenOdd(cur + 2, limit)` to print the next number.
### Step 12:
  Stop
# Program:
#include <stdio.h>

// Function prototypes
int max(int a, int b);
int min(int a, int b);

int main()
{
    int num1, num2;
    int maximum, minimum;

    // Step 4 & 5: Input two numbers
    printf("Enter two numbers: ");
    scanf("%d %d", &num1, &num2);

    // Step 6 & 8: Find maximum
    maximum = max(num1, num2);

    // Step 9 & 11: Find minimum
    minimum = min(num1, num2);

    // Step 12: Display results
    printf("Maximum = %d\n", maximum);
    printf("Minimum = %d\n", minimum);

    return 0;
}

// Step 7: Function to find maximum
int max(int a, int b)
{
    if (a > b)
        return a;
    else
        return b;
}

// Step 10: Function to find minimum
int min(int a, int b)
{
    if (a > b)
        return b;
    else
        return a;
}

# Output:
<img width="487" height="304" alt="image" src="https://github.com/user-attachments/assets/764973b3-0a27-42c5-9707-52b5f229c83f" />

# Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.


# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M5
# IAPR-5- Module 5 - FoC
# Ex.No:24
   Implement a C program that dynamically allocates memory using calloc(), accepts integer inputs from the user, computes their sum, and prints the sum.
# Date : 19/9/2026
# Aim:
  To implement a C program that dynamically allocates memory for an array of integers using calloc(), accepts elements from the user, computes their sum, and displays the sum.
# Algorithm:
### Step 1:
  Start
### Step 2: 
  Include the standard input-output library: #include<stdio.h>. 
### Step 3:
  a. Declare a pointer `ptr` to `int`.  
  b. Declare integers `n`, `i`, and `sum` (initialize `sum = 0`).
### Step 4:
  Read the integer `n` from the user (the number of integers to be stored).
### Step 5:
  Use the `calloc()` function to allocate memory for `n` integers:  
  `ptr = calloc(n, sizeof(int))`
### Step 6:
  If `ptr` is not `NULL`, continue to the next step; otherwise, memory allocation failed (the program exits).
### Step 7:
  For each `i` from `0` to `n - 1`:  
  a. Read an integer from the user.  
  b. Store it at memory location `ptr + i`.
### Step 8:
  For each `i` from `0` to `n - 1`:  
  a. Access the value stored at `ptr + i`.  
  b. Add it to `sum`.
### Step 9:
  Print the value of `sum`.
### Step 10:
  Call `free(ptr);` to release the memory allocated by `calloc()`.
### Step 11:
  Stop
# Program:
#include <stdio.h>

// Step 3: Function prototypes
float celtof();   // Celsius to Fahrenheit
float ftocel();   // Fahrenheit to Celsius

int main()
{
    float F, C;

    // Step 5 & 7: Convert Celsius to Fahrenheit
    F = celtof();
    printf("Temperature in Fahrenheit: %.2f°F\n", F);

    // Step 8 & 10: Convert Fahrenheit to Celsius
    C = ftocel();
    printf("Temperature in Celsius: %.2f°C\n", C);

    return 0;
}

// Step 6: Function to convert Celsius to Fahrenheit
float celtof()
{
    float C, F;
    printf("Enter the temperature in Celsius: ");
    scanf("%f", &C);
    F = (C * 9 / 5) + 32;
    return F;
}

// Step 9: Function to convert Fahrenheit to Celsius
float ftocel()
{
    float f, celsius;
    printf("Enter the temperature in Fahrenheit: ");
    scanf("%f", &f);
    celsius = (f - 32) * 5 / 9;
    return celsius;
}

# Output:
<img width="517" height="289" alt="image" src="https://github.com/user-attachments/assets/29324781-6354-45f6-9398-e132dc93e2bc" />

# Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.


# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M5
# IAPR-5- Module 5 - FoC
# Ex.No:25
   Implement a C program that reads a set of integers into an array and displays the array elements using a user-defined function.
# Date : 
# Aim:
  To implement a C program that reads integers into an array and displays the elements using a user-defined function.
# Algorithm:
### Step 1:
  Start
### Step 2: 
  Include the standard input-output library: #include<stdio.h>. 
### Step 3:
  Declare the function prototype: `void displayArray(int *arr, int size);`
### Step 4:
  In the `main()` function, declare an integer array of size 5 and a loop variable.
### Step 5:
  Prompt the user to enter the required number of integers.
### Step 6:
  Read the integers from the user and store them in the array using a loop.
### Step 7:
  Call the `displayArray` function, passing the array and its size as arguments.
### Step 8:
  Define the function `displayArray(int *arr, int size)` to print the array elements:  
  - Loop through the array using either pointer arithmetic (`*(arr + i)`) or array indexing (`arr[i]`).  
  - Print each element.
### Step 9:
  Return to the `main()` function after displaying the array.
### Step 10:
  Stop
# Program:
#include <stdio.h>
#include <ctype.h>
#include <string.h>

// Step 3: Function definition
void convertFirstCLastC(char str[])
{
    int len = strlen(str);

    if (len == 0)
        return;

    // Convert first character to uppercase
    str[0] = toupper(str[0]);

    // Loop through the string to capitalize characters around spaces
    for (int i = 1; i < len - 1; i++)
    {
        if (str[i] == ' ')
        {
            // Capitalize character before space
            if (i - 1 >= 0)
                str[i - 1] = toupper(str[i - 1]);
            // Capitalize character after space
            if (i + 1 < len)
                str[i + 1] = toupper(str[i + 1]);
        }
    }

    // Convert last character to uppercase
    str[len - 1] = toupper(str[len - 1]);
}

int main()
{
    char str[100];

    // Step 5: Read input string
    printf("Enter a string: ");
    scanf("%[^\n]", str);

    // Call the function to modify the string
    convertFirstCLastC(str);

    // Print the modified string
    printf("Modified string: %s\n", str);

    return 0;
}
# Output:
<img width="405" height="250" alt="image" src="https://github.com/user-attachments/assets/3174cc5a-268e-45f9-b8ce-702856af39e0" />

# Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.
