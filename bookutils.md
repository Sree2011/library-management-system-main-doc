# BookUtils Module

This module provides utility functions for library book management



## Functions

|Function name | Description |
|:--:|:--:|
|`append_dict_to_csv(file_path,my_dict)`|Appends book data into the library csv file|
|`get_books(file_path)`|Gets the list of all books in the library|
|`find_book(file_path,name)`|Finds a book in the library by name|
|`update_book_status(file_path,name,status)`|Updates the status of book by name as "Yes" or "No"|

## Algorithm

1. **Append Dictionary to CSV**
    - **Input**: `file_path`, `my_dict`
    - **Process**:
        - Open the CSV file in append mode.
        - Define the field names for the CSV.
        - Write the dictionary as a new row in the CSV file.
        - Handle any exceptions that occur during file operations.
    - **Output**: None (prints a success message or error message).

2. **Get Books**
    - **Input**: `file_path`
    - **Process**:
        - Read the CSV file into a pandas DataFrame.
        - Convert the DataFrame to a numpy array.
        - Handle any exceptions that occur during file operations.
    - **Output**: A numpy array containing the details of all books.

3. **Find Book**
    - **Input**: `file_path`, `name`
    - **Process**:
        - Call `get_books` to retrieve all books.
        - If no books are found, return an empty DataFrame.
        - Convert the numpy array to a pandas DataFrame.
        - Perform a case-insensitive search for the book by name.
    - **Output**: A pandas DataFrame containing the details of the found book.

4. **Update Book Status**
    - **Input**: `file_path`, `name`, `status`
    - **Process**:
        - Read the CSV file into a numpy array.
        - Perform a case-insensitive search for the book by name.
        - Update the issued status of the found book.
        - Save the updated numpy array back to the CSV file.
    - **Output**: None (updates the CSV file).


## Pseudocode

- [Python](./bookutils-py.md)
- [Java](./bookutils-java.md)
- [C](./bookutils-c.md)