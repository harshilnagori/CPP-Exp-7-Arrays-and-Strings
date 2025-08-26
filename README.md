
 Title      : Pointers in C++
 
 Aim        : To study pointers in C++.
 
 Software   : Visual Studio Code (VS Code)


Objective:
- To understand the concept of pointers in C++.
- To learn how pointers store and manage memory addresses.
- To explore pointer operations such as declaration, initialization, dereferencing.
- To demonstrate the relationship between arrays and pointers.
- To highlight the importance of pointers in dynamic memory allocation.

============================================================================
Theory:

1. Introduction to Pointers:
   - A pointer is a special variable that stores the memory address of another variable.
   - Instead of holding data directly, it "points" to the location where data is stored.
   - Syntax:
        data_type *pointer_name;
     Example:
        int *ptr;

2. Declaring and Initializing Pointers:
   - Declaration: tells the compiler the pointer type.
   - Initialization: assigning the address of a variable using the address-of (&) operator.
     Example:
        int a = 10;
        int *p = &a;   // p stores the address of a

3. Dereferencing Pointers:
   - Dereferencing means accessing the value stored at the memory address
     held by the pointer, using the (*) operator.
     Example:
        cout << *p;   // prints the value stored in 'a'

4. NULL Pointer:
   - A pointer that is not assigned any valid memory address is called a NULL pointer.
   - It points to "nothing".
     Example:
        int *ptr = NULL;

5. Pointer Arithmetic:
   - Since pointers hold addresses, arithmetic operations can be performed:
       - p + 1 → moves to next memory location depending on data type.
       - p - 1 → moves to previous memory location.
     Example:
        If p points to int a[0], then p+1 will point to a[1].

6. Pointers and Arrays:
   - In C++, the name of an array acts like a pointer to its first element.
   - Example:
        int arr[3] = {10, 20, 30};
        int *p = arr;   // p points to arr[0]
        *(p+1) = 20, *(p+2) = 30

7. Pointer to Pointer (Double Pointer):
   - A pointer can store the address of another pointer.
   - Syntax:
        int **pp;
   - Useful in dynamic memory allocation and multi-level referencing.

8. Importance of Pointers:
   - Provide direct access to memory.
   - Enable dynamic memory allocation (malloc/new, free/delete).
   - Essential in data structures like linked lists, trees, and graphs.
   - Useful in function arguments (call by reference).
   - Improve efficiency for large data structures.

============================================================================
 Program: Demonstration of Pointers in C++
============================================================================
*/

#include <iostream>
using namespace std;

int main() {
    // 1. Basic pointer declaration and initialization
    int a = 10;
    int *p = &a;   // pointer p stores the address of a

    cout << "Value of a: " << a << endl;
    cout << "Address of a (&a): " << &a << endl;
    cout << "Pointer p stores: " << p << endl;
    cout << "Value at address stored in p (*p): " << *p << endl;

    // 2. Pointer arithmetic
    int arr[3] = {10, 20, 30};
    int *q = arr;   // pointer to array (points to first element)

    cout << "\nArray elements using pointer arithmetic:" << endl;
    for(int i = 0; i < 3; i++) {
        cout << "arr[" << i << "] = " << *(q + i) << endl;
    }

    // 3. Pointer to pointer
    int **pp = &p;
    cout << "\nPointer to Pointer demonstration:" << endl;
    cout << "Address of p (&p): " << &p << endl;
    cout << "Value stored in pp (address of p): " << pp << endl;
    cout << "Value at *pp (value of p): " << *pp << endl;
    cout << "Value at **pp (value of a): " << **pp << endl;

    // 4. NULL pointer
    int *np = NULL;
    cout << "\nNull pointer np: " << np << endl;

    return 0;
}


SAMPLE OUTPUT :

         To print array elements:
                       Array elements are: 10 20 30 40 50 


         To find number in given array :
                       Enter number to search: 30
                       Found at index 2

         Sum and average of array elements:
                      Enter the numbers of the array:
                      1 2 4 5 6 7 
                      The numbers of the array are:
                      1 2 4 5 6 7 
                      The sum of the elements of the array is:
                      25
                      The average of the elements of the array is: 4.16667


         To find Minimum and maximum Number:
                     Enter the number of elements (1 to 100): 3
                     Enter 3 integers:
                     Enter element 1: 90
                     Enter element 2: 86
                     Enter element 3: 43
                     Minimum value: 43
                     Maximum value: 90

         Declaring & intitalising a string:
                    C-style string: Hello
                    C++ string 1: World
                    C++ string 2: Welcome
                    C++ string 3: World
                    C++ string 4: *****
                    C++ string 5: World to C++
                    C++ string 6: Learning C++ Strings


         Concatenation of strings: 
                    Enter first string: helloooo
                    Enter second string: cutuuuuuuuu
                    Concatenated string: helloooo cutuuuuuuuu

         Printing string in reverse:
                    dlroW olleH

         Palindrome checking:
                    Enter a string: Dad
                    Not a palindrome.

                    
============================================================================
 Conclusion:
- A pointer is a variable that stores the memory address of another variable.
- Pointers allow accessing and manipulating data indirectly using addresses.
- Pointer arithmetic enables traversal of arrays efficiently.
- Pointers can point to other pointers, enabling multiple levels of indirection.
- They are powerful tools for dynamic memory allocation and data structures.
- Mastery of pointers is essential for efficient and advanced C++ programming.
============================================================================
*/

