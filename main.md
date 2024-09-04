# Main Module

This module provides an interactive interface to the user


## Modules

|Module name | Description |
|:--:|:--:|
| `book` | functions to manage a library system, including book management,tracking the issue and return of books, and updating book statuses|

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

**Input**:
- User's name
- User's choice of operation (add a book, list all books, issue a book, return a book)

**Process**:
- Display a welcome message.
- Prompt the user for their name and greet them.
- Display options for adding a book, listing all books, issuing a book, or returning a book.
- Based on the user's choice, call the appropriate function (`add_book`, `list_books`, `issue_book`, `return_book`).

**Output**:
- Execution of the chosen operation.

### Add Book Function

**Input**:
- Book details (name, author, volume)

**Process**:
- Prompt the user to enter the details of the book (name, author, volume).
- Set the issued status to "No".
- Create a `Book` object with the provided details.
- Call the `add_book` method of the `Book` object to add the book to the library.

**Output**:
- Confirmation message that the book has been added.

### List Books Function

**Input**:
- None

**Process**:
- Create a `Book` object with sample data.
- Define column headers as ["Name", "Author", "Volume", "Issued"].
- Call the `get_all_books` method of the `Book` object to retrieve all books.
- Convert the result to a readable format.

**Output**:
- Printed list of all books.
- DataFrame containing the list of all books.

### Issue Book Function

**Input**:
- Name of the book to be issued

**Process**:
- Call the `list_books` function to get the list of all books and store into df.
- Prompt the user to enter the name of the book to be issued.
- Perform a case-insensitive comparison to find the book in df.
- If the book is not found, print "No books found with that name."
- If the book is found, print the details of the book.
- Create a `Book` object using the details of the found book.
- Call the `issue_book` method of the `Book` object to update the issued status to "Yes".

**Output**:
- Confirmation message that the book has been issued.
- Details of the issued book.

### Return Book Function

**Input**:
- Name of the book to be returned

**Process**:
- Call the `list_books` function to get the list of all books and store into df.
- Prompt the user to enter the name of the book to be returned.
- Perform a case-insensitive comparison to find the book in df.
- If the book is not found, print "No books found with that name."
- If the book is found, print the details of the book.
- Create a `Book` object using the details of the found book.
- Call the `return_book` method of the `Book` object to update the issued status to "No".

**Output**:
- Confirmation message that the book has been returned.
- Details of the returned book.

This format clearly outlines the inputs, processes, and outputs for each function, making it easier to understand and implement. If you need further assistance, feel free to ask!

## Pseudocodes

- [Python](./main-py.md)
- [Java](./main-java.md)
- [C](./main-c.md)