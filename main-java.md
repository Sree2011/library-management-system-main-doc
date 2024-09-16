# Main Module - Java

**Modules:**
    - **Book**: The book module defines the functions of a book.\

**Functions:**\
    - **main()**: Displays welcome information to the user.\
    - **add_book():** Adds a new book to the library.\
    - **list_books():** Retrieves a list of all books in the library.\
    - **issue_book(name):** Issues a book and updates its status to "Yes".\
    - **return_book(name):** Returns a book and updates its status to "No".


## Pseudocode

```java

CLASS Main
    DECLARE STATIC OBJECT Scanner sc
    DECLARE STATIC STRING filePath
    ASSIGN "./book-management/src/data/books.txt" to filePath

    METHOD main(String[] args)
        DISPLAY "Hi! Welcome to our Library Book Management System!"
        DISPLAY "What should we call you?"
        DECLARE STRING name_user
        INPUT name_user
        DISPLAY "Hello, " + name_user

        // Display options to the user and take input
        DISPLAY "If you want to add a book, press 1"
        DISPLAY "If you want to see all books, press 2"
        DISPLAY "If you want to get a book issued, press 3"
        DISPLAY "If you want to return a book, press 4"
        DECLARE INTEGER option
        INPUT option

        // EXECUTE OPERATION BASED ON INPUT

        IF option equals 1 THEN
            Call add_book()
            Exit current block
        ELSE IF option equals 2 THEN
            Call list_books()
            Exit current block
        ELSE IF option equals 3 THEN
            Display "Enter the name of the book you want to be issued:"
            Read name from input
            Convert name to lowercase
            Call issue_book(name)
            Exit current block
        ELSE IF option equals 4 THEN
            Display "Enter the name of the book you want to return:"
            Read name from input
            Convert name to lowercase
            Call return_book(name)
            Exit current block
        ELSE
            Display "Invalid input"
        END IF
    END METHOD

    METHOD add_book()
        // Ask for the book details
        DISPLAY "Enter the name of the book to add:"
        DECLARE STRING book_name
        INPUT book_name
        CONVERT book_name to LOWERCASE
        
        DISPLAY "Enter the author of the book to add:"
        DECLARE STRING author_name
        INPUT author_name
        CONVERT author_name to LOWERCASE
        
        DISPLAY "Enter the volume number of the book to add (Eg. 1st, 2nd..):"
        DECLARE STRING volume
        INPUT volume
        CONVERT volume to LOWERCASE
        
        DECLARE STRING issued
        ASSIGN "no" to issued
        

        // Print book details
        DISPLAY "Book Name: " + book_name
        DISPLAY "Author Name: " + author_name
        DISPLAY "Volume: " + volume
        DISPLAY "Issued: " + issued

         // Create a Book object and call the add_book method
        CREATE STATIC OBJECT book Book(book_name,author_name,volume,issued)
        CALL "add_book" method on the "book" object, passing "filePath" as an argument.

    END METHOD

    METHOD list_books()
        CREATE STATIC OBJECT book Book("ff","ss","1st","2nd")
        CALL "get_all_books" method on the "book" object, passing "filePath" as an argument.
    END METHOD

    METHOD issue_book()
        CREATE STATIC OBJECT book Book("ff","ss","1st","2nd")
        CALL "issue_book" method on the "book" object, passing "filePath" as an argument.
    END METHOD

    METHOD return_book()
        CREATE STATIC OBJECT book Book("ff","ss","1st","2nd")
        CALL "return_book" method on the "book" object, passing "filePath" as an argument.
    END METHOD
ENDCLASS

```