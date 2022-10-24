# File I/O

## Opening a File

``` c
FILE *fopen(const char *filename, const char *mode);
```

| Mode | Description                                                                                 |
| :--- | :------------------------------------------------------------------------------------------ |
| r    | Opens a text file for reading.                                                              |
| w    | Opens a text file for writing. Creates a new file if file does not exist.                   |
| a    | Opens a text file for appending. Creates a new file if file does not exist.                 |
| r+   | Opens a text file for both reading and writing. Creates a new file if file does not exist.  |
| w+   | Opens a text file for both reading and writing. Creates a new file if file does not exist.  |
| a+   |  Opens a text file for both reading and writing. Creates a new file if file does not exist. |

## Closing a File

``` c
int fclose(FILE *fp);
```

## Writing to a File

### Write Individual Characters:
``` c
int fputc(int c, FILE *fp);
```

### Write Strings:
``` c
int fputs(const char *s, FILE *fp);

int fprintf(FILE *fp, const char *strings);
```

``` c
#include <stdio.h>

void main() {
   FILE *fp;
   fp = fopen("/tmp/test.txt", "w");
   fprintf(fp, "Writing to file...\n");
   fputs("Also writing to file...\n", fp);
   fclose(fp);
}
```

## Reading from a File

### Read Individual Characters:
``` c
int fgetc(FILE * fp);
```

### Read Strings:
``` c
char *fgets(char *buf, int n, FILE *fp);

int fscanf(FILE *fp, const char *strings);
```

``` c
#include <stdio.h>

void main() {
   FILE *fp;
   char buff[255];

   fp = fopen("/tmp/test.txt", "r");
   fscanf(fp, "%s", buff);
   printf("1 : %s\n", buff );

   fgets(buff, 255, (FILE*)fp);
   printf("2: %s\n", buff );
   
   fgets(buff, 255, (FILE*)fp);
   printf("3: %s\n", buff );
   fclose(fp);
}
```