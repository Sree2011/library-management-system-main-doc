# Main Module - Java

**Modules:**
    - **Book**: The book module defines the functions of a book

**Functions:**
    - **main()**: Displays welcome information to the user
    - **add_book():** Adds a new book to the library.\
    - **list_books():** Retrieves a list of all books in the library.\
    - **issue_book(name):** Issues a book and updates its status to "Yes".\
    - **return_book(name):** Returns a book and updates its status to "No".

## Algorithm

1. **Main Function**
    - Initialize Scanner object for user input.
    - Define file path for storing book data.
    - Display welcome message and ask for user's name.
    - Display options to the user:
        - 1. Add a book
        - 2. List all books
        - 3. Issue a book
        - 4. Return a book
    - Perform operation based on user input using a switch-case structure.

2. **add_book Function**
    - Ask for book details (name, author, volume).
    - Create a Book object with the provided details.
    - Call the `add_book` method of the Book class to add the book to the file.

3. **list_books Function**
    - Create a temporary Book object.
    - Call the `get_all_books` method of the Book class to list all books.

4. **issue_book Function**
    - Ask for the name of the book to be issued.
    - Create a temporary Book object.
    - Call the `issue_book` method of the Book class to issue the book.

5. **return_book Function**
    - Ask for the name of the book to be returned.
    - Create a temporary Book object.
    - Call the `return_book` method of the Book class to return the book.


## Pseudocode

```

Import Scanner

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
        CREATE STATIC OBJECT Book(book_name,author_name,volume,issued)
        Call "add_book" method on the "book" object, passing "filePath" as an argument.

    END METHOD




ENDCLASS

```

