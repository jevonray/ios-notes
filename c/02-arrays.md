# Arrays

## Declaring Arrays
``` c
int arr[10];
```

## Intializing Arrays
``` c
int arr[10] = {1, 2, 3, 4, 5};
```

## Accessing Elements in an Array
``` c
int val = arr[2];
```

## Multi-Dimensional Arrays
``` c
// Declaration
int arr[3][3];

// Initilization
int arr[3][3] = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};

int arr[3][3] = {1, 2, 3, 4, 5, 6, 7, 8, 9};

// Accessing
int val = arr[2][3];
```

## Passing Arrays as Function Arguments
``` c
// As a pointer
void arrFunction(int *arr) {

}

// As a sized array
void arrFunction(int arr[10]) {

}

// As an unsized array
void arrFunction(int arr[]) {

}
```

## Return Array from a Function
``` c
int * arrFunction() {

}
```

## Pointers to Arrays
``` c
int *ptr;
int arr[10];

ptr = arr;
```