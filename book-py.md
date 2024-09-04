**Modules:**\
    - **bookutils:** Manages library system utility functions including book management, tracking issues and returns, and updating book statuses.\
    - **pandas:** Python library for data visualization.\
    - **numpy:** Python library for data analysis.

**Functions:**\
    - **add_book():** Adds a new book to the library.\
    - **find_book(name):** Finds a book by its title.\
    - **get_all_books():** Retrieves a list of all books in the library.\
    - **issue_book(name):** Issues a book and updates its status to "Yes".\
    - **return_book(name):** Returns a book and updates its status to "No".


## Pseudocode

```pseudocode
CLASS Book

    FUNCTION __init__(name, author, volume, issued)
        SET self.name = name
        SET self.author = author
        SET self.volume = volume
        SET self.issued = issued

    FUNCTION add_book()
        CONVERT book attributes to dictionary
        CALL bookutils.append_dict_to_csv with file path and dictionary
        PRINT "Book Added:" and book details

    FUNCTION find_book(name)
        CALL bookutils.find_book with file path and name
        RETURN result as pandas DataFrame

    FUNCTION get_all_books()
        CALL bookutils.get_books with file path
        RETURN result as pandas DataFrame

    FUNCTION issue_book(book_name)
        CALL find_book with book_name
        IF result is empty THEN
            PRINT "No books found with that name."
        ELSE
            CALL bookutils.update_book_status with file path, book_name, "Yes"
            CALL find_book with book_name
            PRINT "Book issued:" and book details

    FUNCTION return_book(name)
        CALL bookutils.update_book_status with file path, name, "No"
        PRINT "Book returned:"
        CALL find_book with name
        PRINT result
```