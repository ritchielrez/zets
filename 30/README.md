# Pointer arithmetic of arrays

Pointer arithmetic of arrays can be bit difficult to understand at first.
Elements of an array stored serially in the memory. Usually if you can get
the address of the 1st element of an array, you can also get memory
access to the other elements. That is how actually arrays are passed to functions
in C. 
Usually the name of the array without `[]` is expressed to the memory address of 
the 1st element of the array. Which means you can store that address in a pointer like this:
```cpp
int arr[] = {1,2,3,4,5};
int *ptr = arr; // ptr now stores the address of the 1st element of arr
```

Guess what is going to get printed in the console after the code is compiled
and run. 
```cpp
#include <iostream>

int main()
{
    int arr[] = {1,2,3,4,5};
    std::size_t size_arr = sizeof(arr);
    int *ptr = arr;

    std::cout << "Size of the arr: " << size_arr << "\n";
    std::cout << ptr << "\n";
    std::cout << ptr + 1 << "\n";
}
```
This is the output in my computer.
```
Size of the arr: 20
000000E2D06FFA88
000000E2D06FFA8C
```
As you can see, the size of the arr is 20 bytes, which makes sense because there 
are 5 integer values stored in the array, and each each integer value is equal to
4 bytes in C.
But see what happens when we try to increment the pointer by 1. Instead of printing
the next memory location, it prints the next memory location of the next element of
the array. You need to remember this, otherwise you may make mistakes in understanding
pointer arithmetic.
Why this happens though, I think when we assign a integer value to the 1st element of
the array, it occupies 4 bytes starting from the address of `000000E2D06FFA88`. 
So in this case we can not point to `000000E2D06FFA89` because a pointer can only point 
to the starting memory address of a variable or an array element.
