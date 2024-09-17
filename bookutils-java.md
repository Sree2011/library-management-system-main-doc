# BookUtils Module - Java

**Modules:**
- **Book** - This is the main class that contains all the utility functions for the library management system.

**Functions:**

- **appendBook(filePath, book):** Adds a new book to the library file.
- **getBooks(filePath):** Retrieves all books from the library file and returns them as a List<Book>.
- **findBook(filePath, name):** Searches for a book by name in the library file and returns the Book object if found.
- **updateBookStatus(filePath,name,status):** Updates the issued status of a book in the library file.

## Pseudocode

```java
CLASS BookUtils

    FUNCTION appendBook(filePath, book)
        TRY
            OPEN file at filePath in append mode
            WRITE book.toString() to file
            WRITE new line to file
        CATCH IOException
            PRINT error message
        END TRY
    END FUNCTION

    FUNCTION getBooks(filePath)
        CREATE empty list called books
        TRY
            OPEN file at filePath for reading
            WHILE there are lines to read
                READ line
                SPLIT line by comma into details array
                IF details array has 4 elements
                    CREATE new Book object with details
                    ADD Book object to books list
                END IF
        CATCH IOException
            PRINT error message
        END TRY
        RETURN books
    END FUNCTION

    FUNCTION findBook(filePath, name)
        books = getBooks(filePath)
        FOR EACH book in books
            IF book.name equals name
                PRINT "Name found: " + book
                RETURN book
            END IF
        PRINT "Name not found."
        RETURN null
    END FUNCTION

    FUNCTION updateBookStatus(filePath, name, status)
        books = getBooks(filePath)
        FOR EACH book in books
            IF book.name equals name
                PRINT "Found book: " + book
                SET book.issued to status
                BREAK loop
            END IF
        END FOR EACH
        
        TRY
            OPEN file at filePath for writing
            FOR EACH book in books
                WRITE book.toString() to file
                WRITE new line to file
        CATCH IOException
            PRINT error message
        END TRY
    END FUNCTION

END CLASS
```