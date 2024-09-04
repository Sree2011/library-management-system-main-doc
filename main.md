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


## Algorithm

### Main Function

    - Display a welcome message.
    - Prompt the user for their name and greet them.
    - Display options for adding a book, listing all books, issuing a book, or returning a book.
    - Based on the user's choice, call the appropriate function (`add_book`, `list_books`, `issue_book`, `return_book`).

### Add Book Function

    - Prompt the user to enter the details of the book (name, author, volume).
    - Set the issued status to "No".
    - Create a `Book` object with the provided details.
    - Call the `add_book` method of the `Book` object to add the book to the library.

### List Books Function

    - Create a `Book` object with sample data.
    - Define column headers as ["Name", "Author", "Volume", "Issued"].
    - Call the `get_all_books` method of the `Book` object to retrieve all books.
    - Convert the result to a readable format.
    - Print and return the result.

### Issue Book Function

    - Call the `list_books` function to get the list of all books and store into df.
    - Prompt the user to enter the name of the book to be issued.
    - Perform a case-insensitive comparison to find the book in df.
    - If the book is not found, print "No books found with that name."
    - If the book is found, print the details of the book.
    - Create a `Book` object using the details of the found book.
    - Call the `issue_book` method of the `Book` object to update the issued status to "Yes".

### Return Book Function

    - Call the `list_books` function to get the list of all books and store into df.
    - Prompt the user to enter the name of the book to be returned.
    - Perform a case-insensitive comparison to find the book in df.
    - If the book is not found, print "No books found with that name."
    - If the book is found, print the details of the book.
    - Create a `Book` object using the details of the found book.
    - Call the `return_book` method of the `Book` object to update the issued status to "No".


## Pseudocodes

### Python

**Modules:**
    - **book:** Manages library system functionalities including book management, tracking issues and returns, and updating book statuses.
    - **pandas:** Python library for data visualization.
    - **numpy:** Python library for data analysis.

**Functions:**
    - **add_book():** Adds a new book to the library.
    - **find_book(name):** Finds a book by its title.
    - **list_books():** Retrieves a list of all books in the library.
    - **issue_book(name):** Issues a book and updates its status to "Yes".
    - **return_book(name):** Returns a book and updates its status to "No".

```pseudocode
FUNCTION main
    PRINT welcome message
    PROMPT user for their name and greet them
    DISPLAY options for adding a book, listing all books, issuing a book, or returning a book
    READ user input as option
    IF option is 1 THEN
        CALL add_book
    ELSE IF option is 2 THEN
        CALL list_books
    ELSE IF option is 3 THEN
        CALL issue_book
    ELSE IF option is 4 THEN
        CALL return_book

FUNCTION add_book
    PRINT prompt for book details
    READ book name, author, and volume from user input
    SET issued status to "No"
    CREATE a Book object with the provided details
    CALL add_book method of the Book object

FUNCTION list_books
    CREATE a Book object with sample data
    DEFINE column headers as ["Name", "Author", "Volume", "Issued"]
    CALL get_all_books method of the Book object
    CONVERT result to a pandas DataFrame with specified columns
    SET DataFrame index to start from 1
    PRINT the DataFrame
    RETURN the DataFrame

FUNCTION issue_book
    CALL list_books and store result in df
    PROMPT user to enter the name of the book to be issued
    READ user input as name
    FILTER df for rows where "Name" matches user input (case-insensitive)
    IF result is empty THEN
        PRINT "No books found with that name."
    ELSE
        PRINT "Books found:" and the result
        CREATE a Book object using data from the first row of the result
        CALL issue_book method of the Book object with user input

FUNCTION return_book
    CALL list_books and store result in df
    PROMPT user to enter the name of the book to be returned
    READ user input as name
    FILTER df for rows where "Name" matches user input (case-insensitive)
    IF result is empty THEN
        PRINT "No books found with that name."
    ELSE
        PRINT "Books found:" and the result
        CREATE a Book object using data from the first row of the result
        CALL return_book method of the Book object with user input
```

