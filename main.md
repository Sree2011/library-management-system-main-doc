# Main Module

This module provides an interactive interface to the user

Modules:

    book: 
        functionalities to manage a library system, including book management, tracking the issue and return of books, and updating book statuses

> import other dependencies based on the language chosen
    
Functions:

    main():
      A user interface
      
    add_book(): 
        Adds a new book to the library.

    find_book(name): 
        Finds a book by its title.

    list_books(): 
        Retrieves a list of all books in the library.

    issue_book(name): 
        Issues a book and updates its status to "Yes".
        
    return_book(name): 
        Returns a book and updates its status to "No".



## Main function
  Display welcome information to the user and
  do the operation based on the user's preference

  **Parameters:**\
      None
      
  **Returns:**\
      None
        
```pseudocode
FUNCTION main()
    DISPLAY "Hi! Welcome to our Library Book Management System!"
    DISPLAY "What should we call you?"
    DECLARE STRING name_user
    INPUT name_user
    DISPLAY "Hello, " + name_user
    DECLARE INTEGER option
    DISPLAY "If you want to add a book, press 1"
    DISPLAY "If you want to see all books, press 2"
    DISPLAY "If you want to get a book issued, press 3"
    DISPLAY "If you want to return a book, press 4"
    INPUT option
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
