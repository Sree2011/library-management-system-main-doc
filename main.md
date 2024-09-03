# Main Module

This module provides an interactive interface to the user

## Main function

```pseudocode
FUNCTION main()
  '''
    Display welcome information to the user and
    do the operation based on the user's preference

    Parameters:
        None
    Returns:
        None
  '''
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
