# Main Module

This module provides an interactive interface to the user


## Modules

    book: 
        functionalities to manage a library system, including book management, tracking the issue and return of books, and updating book statuses

> import other dependencies based on the language chosen

    
## Functions

|Function name | Description |
|:--:|:--:|
|`main()`|A user interface|
|`add_book()`|Adds a new book to the library|
|`find_book(name)`|Finds a book by its title|
|`list_books()`|Gets the list of all books in the library|
|`issue_book(name)`|Issues a book and updates its status to "Yes"|
|`return_book(name)`|Returns a book and updates its status to "No"|


### Main function
  Display welcome information to the user and
  do the operation based on the user's preference

  **Parameters:**\
      None
      
  **Returns:**\
      None
        
```pseudocode
FUNCTION main()
    # Welcome the user and ask name
    DISPLAY "Hi! Welcome to our Library Book Management System!"
    DISPLAY "What should we call you?"
    DECLARE STRING name_user
    INPUT name_user
    DISPLAY "Hello, " + name_user
    DECLARE INTEGER option

    # Display options to the user and take input
    DISPLAY "If you want to add a book, press 1"
    DISPLAY "If you want to see all books, press 2"
    DISPLAY "If you want to get a book issued, press 3"
    DISPLAY "If you want to return a book, press 4"
    INPUT option

    # Perform operation based on the input
    IF option is equal to 1
      CALL add_book()
    ELSE IF option is equal to 2
      CALL list_books()
    ELSE IF option is equal to 3
      CALL issue_book()
    ELSE IF option is equal to 4
      CALL return_book()
    ENDIF
  END FUNCTION
```

### Add Book function

Take the details of the book from the user as input
and add them to the library file.

  **Parameters:**\
      None
      
  **Returns:**\
      None

```pseudocode
FUNCTION add_book()
    # Get the details from the user
    DISPLAY "Enter the details of the book you want to add:"
    DECLARE STRING name_book
    DECLARE STRING author_book
    DECLARE STRING volume_book
    DECLARE STRING issued
    
    INPUT name_book
    name_book = CAPITALIZE(name_book)
    
    INPUT author_book
    author_book = CAPITALIZE(author_book)
    
    INPUT volume_book
    
    issued = "No"
    
    # Create an object of Book class from book module to activate functions
    DECLARE OBJECT new_book
    new_book = CREATE Book(name_book, author_book, volume_book, issued)
    
    # Call the add book function
    CALL new_book.add_book()
```
