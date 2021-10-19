# Software Requirements Specification of programm "Library"

1. Introduction
	- Purpose
	- Project scope
2. Overall description
	- Books
		+ View a list of books
		+ Add a book
		+ Edit a book
		+ Delete a book
	- Readers
		+ View a list of readers
		+ Add a reader
		+ Edit a reader
		+ Delete a reader

## 1. INTRODUCTION

### 1.1 Purpose

The purpose of this document is to build an online system to manage books and readers.

### 1.2 Project scope

The purpose of the library management system is to ease books and readers management and to create a convenient and easy-to-use application. The application must implement the following functions:

- view a list of all books
- add a book
- edit a book
- delete a book
- view a list of all readers
- add a reader
- edit a reader
- delete a reader
- view the number of issued books
- selection of a book using a filter by name

## 2. Overall description

### 2.1 Books

#### 2.1.1 View a list of books

This application mode allows you to view the list of books and the number of issued books. 

Main script:

* the user selects the menu item "Books"
* the form for viewing the list of all books is displayed

image1

The list displays the following columns:

* title - title of the book
* number of issued books
* description - description of the book

**Search:**

* it is possible to search by the title of the book
* search after entering the name is carried out by clicking the "Search" button



#### 2.1.2 Add a book

Main script:

* in the book view mode, click "Add" button 
* a form for adding a new book is displayed
* the user enters data(book title, description) and clicks "Save" button 
* if the data is entered incorrectly, then a notification about incorrect data is displayed
* if the data is correct, then the book is added to the database
* if an error occurred while saving data, the error message "Error saving data" is displayed
* if the book is successfully added, then the form for viewing all books opens

Cancellation script:

* in the book view mode, click "Add" button 
* a form for adding a new book is displayed
* the user enters data(book title, description) and clicks "Cancel" button 
* data is not saved to the database and a form for viewing all books opens

image2

#### 2.1.3 Edit a book

Main script:

* in the book view mode, click "Edit" button in the row of the selected book
* editing form is displayed
* the user changes data(book title, description) and clicks "Save" button
* if the data is entered incorrectly, then a notification about incorrect data is displayed
* if the data is correct, then the data is updated in the database
* if an error occurred while saving data, the error message "Error saving data" is displayed
* if the book is successfully updated, then the form for viewing all books opens

Cancellation script:

* in the book view mode, click "Edit" button in the row of the selected book
* editing form is displayed
* the user changes data and clicks "Cancel" button
* data is not saved to the database and a form for viewing all books opens

image3

**Data validation constraints:**

* book title - length no more than 50 characters, value should be unique
* the length of the description value is not more than 1000 characters

#### 2.1.4 Delete a book

Main script:

* in the book view mode, click "Delete" button in the row of the selected book
* there is a check for the ability to delete the book, if this book is not used by any users
* if the book is in use, the warning "This book cannot be deleted, as there is a connection with the user"
* if the book can be deleted, a warning dialog is displayed "Please confirm to delete the book: *book title*"
* the user clicks "Delete" button
* the book is deleted in the database
* if an error occurred while deleting data, the error message "Data deleting error" is displayed
* if the book is successfully deleted, then the form for viewing all books opens

Cancellation script:

* in the book view mode, click "Delete" button in the row of the selected book
* if the book can be deleted, a warning dialog is displayed "Please confirm to delete the book: *book title*"
* the user clicks "Cancel" button
* the form for viewing all books opens

image4

### 2.2 Readers

#### 2.2.1 View a list of readers

This application mode allows you to view the list of readers.

Main script:

* the user selects the menu item "Readers"
* the form for viewing the list of all readers is displayed

image5

The list displays the following columns:

* first name - first name of the reader
* second name - second name of the reader
* book title

#### 2.2.2 Add a reader

Main script:

* in the reader view mode, click "Add" button 
* a form for adding a new reader is displayed
* the user enters data(first name, second name, book title) and clicks "Save" button 
* if the data is entered incorrectly, then a notification about incorrect data is displayed
* if the data is correct, then the reader is added to the database
* if an error occurred while saving data, the error message "Error saving data" is displayed
* if the reader is successfully added, then the form for viewing all readers opens

Cancellation script:

* in the reader view mode, click "Add" button 
* a form for adding a new reader is displayed
* the user enters data(first name, second name, book title) and clicks "Cancel" button 
* data is not saved to the database and a form for viewing all readers opens

image6

#### 2.2.3 Edit a reader

Main script:

* in the reader view mode, click "Edit" button in the row of the selected reader
* editing form is displayed
* the user changes data(first name, second name, book title) and clicks "Save" button
* if the data is entered incorrectly, then a notification about incorrect data is displayed
* if the data is correct, then the data is updated in the database
* if an error occurred while saving data, the error message "Error saving data" is displayed
* if the reader is successfully updated, then the form for viewing all readers opens

Cancellation script:

* in the reader view mode, click "Edit" button in the row of the selected reader
* editing form is displayed
* the user changes data and clicks "Cancel" button
* data is not saved to the database and a form for viewing all readers opens

image7

**Data validation constraints:**

* first name - required field, length no more than 100 characters
* last name - required field, length no more than 100 characters
* book title - one value is selected from the list of available books, if there is no book in the system, then a new reader cannot be added

#### 2.2.4 Delete a reader

Main script:

* in the reader view mode, click "Delete" button in the row of the selected reader
* a warning dialog is displayed "Please confirm to delete the reader: *user`s first and second name*"
* the user clicks "Delete" button
* the reader is deleted in the database
* if an error occurred while deleting data, the error message "Data deleting error" is displayed
* if the reader is successfully deleted, then the form for viewing all readers opens

Cancellation script:

* in the reader view mode, click "Delete" button in the row of the selected reader
* a warning dialog is displayed "Please confirm to delete the book: *user`s first and second name*"
* the user clicks "Cancel" button
* the form for viewing all readers opens

image8
	
