# Book Module - Java

**Modules:**\
    - **bookutils:** Manages library system utility functions including book management, tracking issues and returns, and updating book statuses.

**Functions:**\

1. **Constructor:**
   - **Book(name,author,volume,issued):** Creates a book object with given parameters

2. **Getter and Setter Methods:**
   - **getName():** Returns the value of the `name` instance variable
   - **getAuthor():** Returns the value of the `author` instance variable
   - **getVolume():** Returns the value of the `volume` instance variable
   - **getIssued():** Returns the value of the `issued` instance variable

   - **setName(name):** Sets the value of the `name` instance variable with provided `name` argument
   - **setAuthor(author):** Sets the value of the `author` instance variable with provided `author` argument
   - **setVolume(volume):** Sets the value of the `volume` instance variable with provided `volume` argument
   - **setIssued(issued):** Sets the value of the `issued` instance variable with provided `issued` argument


3. **Library Management Methods:**
   - **add_book():** Adds a new book to the library.\
    - **list_books():** Retrieves a list of all books in the library.\
    - **issue_book(name):** Issues a book and updates its status to "Yes".\
    - **return_book(name):** Returns a book and updates its status to "No".

## Pseudocode

```java
CLASS Book
    PRIVATE name AS STRING
    PRIVATE author AS STRING
    PRIVATE volume AS STRING
    PRIVATE issued AS STRING

    METHOD Book(name AS STRING, author AS STRING, volume AS STRING, issued AS STRING)
        SET this.name TO name
        SET this.author TO author
        SET this.volume TO volume
        SET this.issued TO issued
    END METHOD

    METHOD getName() RETURNS STRING
        RETURN name
    END METHOD

    METHOD setName(name AS STRING)
        SET this.name TO name
    END METHOD

    METHOD getAuthor() RETURNS STRING
        RETURN author
    END METHOD

    METHOD setAuthor(author AS STRING)
        SET this.author TO author
    END METHOD

    METHOD getVolume() RETURNS STRING
        RETURN volume
    END METHOD

    METHOD setVolume(volume AS STRING)
        SET this.volume TO volume
    END METHOD


    METHOD add_book(filePath AS STRING)
        CALL appendBook FUNCTION FROM BookUtils MODULE BY PASSING filePath AS ARGUMENT
    END METHOD

    METHOD get_all_books(filePath AS STRING) RETURNS List<Book>
        RETURN VALUE OF getBooks FUNCTION FROM BookUtils MODULE BY PASSING filePath AS ARGUMENT
    END METHOD

    METHOD issue_book(filePath AS STRING, name AS STRING)
        CALL updateBookStatus FUNCTION FROM BookUtils MODULE BY PASSING filePath,name AND "yes" AS ARGUMENTS
        PRINT "Book issued: " + name
    END METHOD

    METHOD return_book(filePath AS STRING, name AS STRING)
        CALL updateBookStatus FUNCTION FROM BookUtils MODULE BY PASSING filePath,name AND "no" AS ARGUMENTS
        PRINT "Book returned: " + name
    END METHOD

END CLASS

```