# Main Module

This module provides an interactive interface to the user

FUNCTION main()
  '''
    Display welcome information to the user and
    do the operation based on the user's preference

    Parameters:
        None
    Returns:
        None
  '''
  DISPLAY list of options 1,2,3,4
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
