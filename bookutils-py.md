# BookUtils Module - Python

**Modules:**\
    - **csv:** Python library for handling csv files.\
    - **pandas:** Python library for data visualization.\
    - **numpy:** Python library for data analysis.

**Functions:**\
    - **append_dict_to_csv(file_path,my_dict):** Appends book data into the library csv.\
    - **find_book(file_path,name):** Finds a book by its title.\
    - **get_books(file_path):** Retrieves a list of all books in the library.\
    - **update_book_status(file_path,name,status):** Issues a book and updates its status to "Yes".\



### Pseudocode

```java
FUNCTION append_dict_to_csv(file_path, my_dict)
    TRY
        OPEN file_path in append mode as file
        DEFINE fieldnames as ['name', 'author', 'volume', 'issued']
        CREATE a DictWriter object with file and fieldnames
        WRITE my_dict to the CSV file
        PRINT success message
    EXCEPT Exception as e
        PRINT error message
    END TRY
END FUNCTION


FUNCTION get_books(file_path)
    TRY
        READ CSV file_path into a pandas DataFrame
        CONVERT DataFrame to numpy array
        RETURN numpy array
    EXCEPT Exception as e
        PRINT error message
        RETURN empty numpy array
    END TRY
END FUNCTION

FUNCTION find_book(file_path, name)
    CALL get_books(file_path) and store result in books
    IF books is empty THEN
        RETURN empty DataFrame with columns ["Name", "Author", "Volume", "Issued"]
    CONVERT books to pandas DataFrame with columns ["Name", "Author", "Volume", "Issued"]
    CONVERT name to lowercase
    FILTER DataFrame for rows where "Name" matches name (case-insensitive)
    RETURN filtered DataFrame
END FUNCTION

FUNCTION update_book_status(file_path, name, status)
    READ CSV file_path into a numpy array, skipping header
    CONVERT name to lowercase
    FIND positions in numpy array where "Name" matches name (case-insensitive)
    FOR each position in positions
        UPDATE issued status to status
    SAVE updated numpy array back to CSV file_path with header
END FUNCTION

```