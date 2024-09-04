# Book Module

This module initialises a book class and calls the utility functions from bookutils module

## Modules

|Module name | Description |
|:--:|:--:|
| `bookutils` | utility functions to manage a library system, including book management,tracking the issue and return of books, and updating book statuses|

> import other dependencies based on the language chosen

## Classes

|Class name | Description |
|:--:|:--:|
|Book| A class for adding books with required parameters|

## Functions

|Function name | Description |
|:--:|:--:|
|`Book(name,author,volume,issued)`|Constructor of Book class|
|`add_book()`|Adds a new book to the library|
|`find_book(name)`|Finds a book by its title|
|`get_all_books()`|Gets the list of all books in the library|
|`issue_book(name)`|Issues a book and updates its status to "Yes"|
|`return_book(name)`|Returns a book and updates its status to "No"|


### Algorithm

1. **Book Class Initialization**
    - **Input**: `name`, `author`, `volume`, `issued`
    - **Process**: Initialize the `Book` object with the provided attributes.
    - **Output**: A `Book` object.

2. **Add Book**
    - **Input**: None
    - **Process**:
        - Convert the book's attributes to a dictionary.
        - Append the dictionary to a CSV file using `bookutils.append_dict_to_csv`.
        - Print the details of the added book.
    - **Output**: None

3. **Find Book**
    - **Input**: `name`
    - **Process**:
        - Use `bookutils.find_book` to search for the book in the CSV file.
        - Return the result as a pandas DataFrame.
    - **Output**: A pandas DataFrame containing the details of the found book.

4. **Get All Books**
    - **Input**: None
    - **Process**:
        - Use `bookutils.get_books` to retrieve all books from the CSV file.
        - Return the result as a pandas DataFrame.
    - **Output**: A pandas DataFrame containing the details of all books.

5. **Issue Book**
    - **Input**: `book_name`
    - **Process**:
        - Call `find_book` to search for the book.
        - If the book is not found, print a message.
        - If the book is found, update the "issued" status to "Yes" using `bookutils.update_book_status`.
        - Print the details of the issued book.
    - **Output**: None

6. **Return Book**
    - **Input**: `name`
    - **Process**:
        - Update the "issued" status to "No" using `bookutils.update_book_status`.
        - Print a message indicating the book has been returned.
        - Call `find_book` to retrieve and print the details of the returned book.
    - **Output**: None

### Pseudocode


- [Python](./book-py.md)
- [Java](./book-java.md)
- [C](./book-c.md)