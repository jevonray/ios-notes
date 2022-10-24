# Dynamic Memory Allocation

## Functions

| Function                                     | Description                                                                  |
| :------------------------------------------- | :--------------------------------------------------------------------------- |
| void *calloc(int num, int size);             | Allocates an array of num elements each of which size in bytes will be size. |
| void *malloc(size_t size);                   | Allocates an array of num bytes and leave them uninitialized.                |
| void *realloc(void *address, int newsize);   | Reallocates memory extending it upto newsize.                                |
| void free(void *address);                    | Releases a block of memory block specified by address.                       |

## Allocating Memory Dynamically

``` c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main() {

   char *dynamicArray;
   dynamicArray = malloc(50 * sizeof(char)); // size 50

   strcpy(dynamicArray, "This is a test string in a dynamic array");
   
   dynamicArray = realloc(dynamicArray, 100 * sizeof(char)); // size 100

   free(description);

   return 0;
}
```