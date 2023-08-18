# How to pass arrays into functions and print them in C

Right at the start, let's explain why code the below does not work.
```cpp
#include <iostream>

void printarr(int arr[])
{
    for(const int &e : arr)
    {
        std::cout << e << " ";
    }
    std::cout << "\n";
}

int main()
{
    int arr[] { 1, 2, 3, 4, 5, 6 , 7};

    printarr(arr);
}
```

In C and C++, we can pass arrays to functions by their memomy address, and inside functions use the passed array 
as if the array was declared inside of the function, no need to use the dereference operator. But there is a catch.
Arrays as passed into as pointers. Range based loops require actual arrays to iterate through. In case of arrays being
passed as pointers, we need to use the old way of iterating through an array.
```cpp
#include <iostream>

void printarr(int arr[], std::size_t size)
{
    for(std::size_t i = 0; i < size; ++i)
    {
        std::cout << arr[i] << " ";
    }
    std::cout << "\n";
}

int main()
{
    int arr[] { 1, 2, 3, 4, 5, 6 , 7};
    std::size_t size_arr = sizeof(arr) / sizeof(arr[0]);

    printarr(arr, size_arr);
}
```

