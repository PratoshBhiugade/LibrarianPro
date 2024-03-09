# Library Management System Repository Documentation
# Overview
The Library Management System (LMS) repository is a comprehensive Application solution designed to automate and streamline the operations of libraries. It serves as a centralized platform for managing library resources efficiently, including books, journals, multimedia materials, and user information.
# Project Structure
**The repository is organized into several components, each serving a specific purpose within the system:**

**1.Model:** Contains the data models representing library resources, such as books, users, and transactions.

**2.Controller:** Implements the business logic for managing library resources, including CRUD operations (Create, Read, Update, Delete) on books, users, and transactions.

**3.View:** Provides the user interface for interacting with the system, including features for browsing the catalog, borrowing books, and managing user accounts.


# Components

# 1. Controller

# Here's a description for the provided controller class:

**Package:** com.qsp.lms_controller

**Class Name:** controller

**Description:**
The controller class serves as the intermediary between the user interface (view) and the data model (model) components of the Library Management System (LMS). It encapsulates the business logic for managing the library's collection of books. This class provides methods for adding, retrieving, updating, and removing books from the library.

**Methods:**

addBook(book Book):
Adds a new book to the library's collection.

**Parameters:**
Book: The book object to be added to the library.

**Behavior:**
If the list of books is null, initializes it as a new ArrayList.
Adds the provided book to the list of books.
Updates the library's book collection.

**getBook(String bookName):**

Retrieves a book from the library by its name.

**Parameters:**
bookName: The name of the book to retrieve.

**Returns:**
The book object if found, or null if not found.

**Behavior:**
Iterates through the list of books.
Compares the name of each book with the provided bookName (case-insensitive).
Returns the book object if a match is found, otherwise returns null.

**updateBook(book bookExit, book bookUpdate):**

Updates an existing book in the library with new information.

**Parameters:**
bookExit: The book to be updated (original book object).
bookUpdate: The updated information for the book (new book object).

**Returns:**
true if the book was successfully updated, false otherwise.

**Behavior:**
Iterates through the list of books.
Finds the book to be updated based on its name.
Removes the original book from the list and adds the updated book.
Returns true if the update was successful, false otherwise.

**removeBook(String bookName):**

Removes a book from the library by its name.

**Parameters:**
bookName: The name of the book to remove.

**Returns:**
true if the book was successfully removed, false otherwise.

**Behavior:**
Iterates through the list of books.
Finds the book to be removed based on its name.
Removes the book from the list if found.
Returns true if the removal was successful, false otherwise.

# 2. Model

# Below is the documentation for the book class:

**Package:** com.qsp.lms_model

**Class Name:** book

**Description:**

The book class represents a book in the library management system. It encapsulates information about a book, including its name, author, and price.

**Fields:**

bookName: The name of the book.
bookAuther: The author of the book.
bookPrice: The price of the book.

**Methods:**

**getBookName(): String**

Returns the name of the book.
Return Type: String

**setBookName(String bookName): void**

Sets the name of the book.
Parameters:
bookName (String): The name of the book.
Return Type: void

**getBookAuther(): String**

Returns the author of the book.
Return Type: String

**setBookAuther(String bookAuther): void**

Sets the author of the book.
Parameters:
bookAuther (String): The author of the book.
Return Type: void

**getBookPrice(): double**

Returns the price of the book.
Return Type: double

**setBookPrice(double bookPrice): void**

Sets the price of the book.
Parameters:
bookPrice (double): The price of the book.
Return Type: void

**toString(): String**

Returns a string representation of the book.
Return Type: String
Format: "bookName = [bookName], bookAuther = [bookAuther], bookPrice = [bookPrice]"



# here's the documentation for the library class:


**Package:** com.qsp.lms_model

**Class Name:** library

**Description:**

The library class represents a library in the library management system. It encapsulates information about a library, including its name, address, pin code, and the list of books it contains.

**Fields:**

libraryName: The name of the library.
libraryAddress: The address of the library.
libraryPinCode: The pin code of the library.
books: A list of books available in the library.
Methods:

**getLibraryName(): String**

Returns the name of the library.
Return Type: String

**setLibraryName(String libraryName): void**

Sets the name of the library.
Parameters:
libraryName (String): The name of the library.
Return Type: void

**getLibraryAddress(): String**

Returns the address of the library.
Return Type: String

**setLibraryAddress(String libraryAddress): void**

Sets the address of the library.
Parameters:
libraryAddress (String): The address of the library.
Return Type: void

**getLibraryPinCode(): int**

Returns the pin code of the library.
Return Type: int

**setLibraryPinCode(int libraryPinCode): void**

Sets the pin code of the library.
Parameters:
libraryPinCode (int): The pin code of the library.
Return Type: void

**getBooks(): List<book>**

Returns the list of books available in the library.
Return Type: List<book>

**setBooks(List<book> books): void**

Sets the list of books available in the library.
Parameters:

**books (List<book>): The list of books available in the library.**

Return Type: void

# 3. View
# here's the documentation for the view class:

**Package:** com.qsp.lms_view

**Class Name:** view

**Description:**

The view class serves as the user interface for the Library Management System (LMS). It interacts with the user through the console, allowing them to perform various operations such as adding, retrieving, updating, and removing books from the library's collection.

**Fields:**

Library: An instance of the library class representing the library in the system.

**Methods:**

**getLibrary(): library**

Returns the library object.
Return Type: library

**setLibrary(library library): void**

Sets the library object.
Parameters:
library (library): The library object to set.
Return Type: void

**main(String[] args): void**

The main method of the view class, responsible for starting the user interface and handling user input.
Parameters:
args (String[]): Command-line arguments (not used in this implementation).
Return Type: void

**Usage:**

The main method initializes the library by prompting the user to enter the library's name, address, and pin code.

It then displays a menu of options for the user to perform various operations on the library's collection of books.

Based on the user's choice, it invokes methods from the controller class to add, retrieve, update, or remove books.

The user can continue interacting with the system until they choose to exits.

# How to Run
**1.Compile and Run:**

javac.com/jsp/lms/view/view.java,
java.com/jsp/lms/view/view

**2.Follow On-screen Prompts:**

Enter library details during initialization.
Choose option to add,remove,update,or get book details.

# Use Cases

 **To Add Book**

 ![add](https://github.com/PratoshBhiugade/LibrarianPro/assets/104575164/1a8af4f4-cf59-4b0d-95ca-a2d62debf44c)

 
  **To Update Book**
 
 ![image](https://github.com/PratoshBhiugade/LibrarianPro/assets/104575164/e3a82f3b-04d8-484a-8419-80e3611ee783)

 
 **To Fetch Book**

 ![fetch](https://github.com/PratoshBhiugade/LibrarianPro/assets/104575164/cd3ef76e-a68e-475b-b25a-72344cd8c6f1)


 **To Remove Book**

 ![remove](https://github.com/PratoshBhiugade/LibrarianPro/assets/104575164/5ac7c37c-6f96-4fbd-a180-cb7733f8a3f9)


**To Exit Book**

 ![image](https://github.com/PratoshBhiugade/LibrarianPro/assets/104575164/575029fc-2dba-4437-ba46-dee5ac4b43c6)


