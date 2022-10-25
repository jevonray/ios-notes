# Command Line Arguments

``` c
// argc - number of arguments passed
// argv -  pointer array to arguments passed
int main(int argc, char *argv[]) 
```

``` c
// test.c

#include <stdio.h>

int main(int argc, char *argv[])  {

   printf(argc);

   printf(argv[0]);

   printf(argv[1]);

   return 0;
}
```

```
$./test test1 test2
2
test1
test2
```