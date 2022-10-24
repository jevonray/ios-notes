# Structures

## Defining a Structure
``` c
struct Books {
   char  title[50];
   char  author[50];
   char  subject[100];
   int   bookId;
};  
```

## Declaring a Structure
``` c
struct Book book1;
```

## Accessing Structure Members
``` c
strcpy(book1.title, "The C Programming Language");
strcpy(book1.author, "Kernighan and Ritchie");
strcpy(book1.subject, "Computer Science");
book1.bookId = 1234;

printf("Book 1 Title: %s\n", book1.title);
printf("Book 1 Author: %s\n", book1.author);
printf("Book 1 Subject %s\n", book1.subject);
printf("Book 1 ID: %d\n", book1.bookId);
```

## Passing Structure as Function Arguments
``` c
void structFunction(struct Book book1) {

}
```

## Pointers to Structures
``` c
// Define pointer
struct Books *structPtr;

// Declar pointer
structPtr = &book1;

// Access structure pointer members
structPtr->title;
structPtr->author;
structPtr->subject;
structPtr->bookId;
```