# Pointers

## Declaring Pointers
``` c
int *intPtr;   
```

## Storing Address in Pointers
``` c
int val = 5;
intPtr = &val;
```

## NULL Pointers
``` c
int *ptr = NULL;
printf("Output: %x\n", ptr); // Output: 0
```

## Pointer Arithmetic
``` c
// Increment
intPtr++;

// Decrement
intPtr--;

// Comparison
intPtr == &val;
intPtr < &val;
intPtr > &val
intPtr >= &val;
intPtr <= &val;
```

## Array of Pointers
``` c
int  val[] = {1, 2, 3, 4, 5};
int *arrPtr[5];
 
for (int i = 0; i < 5; i++) {
    intPtr[i] = &val[i];
}
```

## Pointer to Pointer
``` c
int val = 5;
int *ptr = &val;
int **ptrPtr = &ptr;
```
## Passing Pointers as Function Arguments
``` c
int val = 0;
ptrFunction(&val);

void ptrFunction(int *ptr) {

}

// Note: functions that accept pointers can also accept arrays.
int vals[5] = {1, 2, 3, 4, 5};
ptrFunction(vals);
```

## Return Pointers from a Function
``` c
int * ptrFunction() {

}
```V