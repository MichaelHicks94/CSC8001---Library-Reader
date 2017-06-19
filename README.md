# CSC8001---Library-Reader

My third project for CSC8001 (Programming and Data Structures). The goal of the project was to build an interface to simulate a library, which can loan and return books to, and from, people and store information about the books in the library. The aims of the project was to gain experience at designing interactive systems, to reinforce knowledge about the standard java.util.ArrayList<E> ckass and to gain experience in using the java.lang.Comparable<E> interface as well as using inheritance and generic classes in Java.

Specification:

Task 1:
Derive a SortedArrayList<E> class from the java.util.ArrayList<E> class in
such a way that the items of a sorted array list are sorted in ascending order. This subclass of
ArrayList<E> class will be needed to complete Task 2 (see Additional assumptions (2)
below). For simplicity, you can provide only your new insertion method in the
SortedArrayList<E> class. It is not a part of this project to consider all the mutator
methods from ArrayList<E> class and see whether/how they should be overridden to
make sure that a sorted list preserves its order when they are invoked on the list.

Task 2:
You are asked to write a program to help a librarian in their daily work. Your program should
read a list of books and a list of users from a file. The content of the input file should have the
following form: The first line contains an integer representing the number of books in the
library, and is followed by the information about the books (two lines for every book: one
line containing the title and the second one containing the author’s name). The next line
contains an integer representing the number of library users, followed by the information
about the users (one line for every user with their first name and surname). Example file
content is given below:

5
Concurrent Programming
C. R. Snow
Concurrent Programming
Stephen J. Hartley
Java Gently
Judith Bishop
Petri Nets
Wolfgang Reisig
Finite Transition Systems
Andre Arnold
4
Anna Smith
Zoe Brown
John Williams
John Smith

The program should be able to store the information about books and users:
1. For each book, the information required is: the title, author’s name, whether it is on
loan or not, and if it is on loan, who borrowed it. We assume that every book has only
one author and that there are no two books in the library with the same title and
author.
2. For each user, the library should know the first name, surname and the number of
books currently held by the user. We assume that at any time a user can hold at most 3
books. We also assume that no two users share both the first name and the surname.
After the initial information has been read from the file, the librarian will be working with the
program interactively. The program should display a menu on the screen offering a choice of
possible operations, each represented by a lower case letter:
 f - to finish running the program.
 b - to display on the screen the information about all the books in the library.
 u - to display on the screen the information about all the users.
 i - to update the stored data when a book is issued to a user.
 r - to update the stored data when a user returns a book to the library.
You should implement all the above operations.

Additional assumptions:
1. When f is selected, the program stops running and all the data are lost. The program
could be extended to save all the data to a file, but this is not a part of the project!
2. To store books and users you should use SortedArrayList<E> class. Books
should be sorted in the ascending order of surnames of authors. You can assume that
each author has only one surname and that it is always given after the first name(s)
and/or initial(s). If there are several books by authors with the same surname, their
order in the sorted list is not important. Users should be sorted in the ascending order
of their surnames. If two users have the same surname then the first names should
decide their order. You can assume that each user has exactly one first name and
exactly one surname.
3. When a book is to be issued to a user, it must be checked whether the user is a valid
user, and that the book is on the list of the books in the library. If not, an appropriate
message should be displayed on the screen. If the request is a valid one, the program
should check whether the book is on loan or not. If the book is currently on loan, a
note to the user who is holding the book should be printed to a file informing that the
book was requested by another user and should be returned as soon as possible. If the
book is available, the stored information should be updated accordingly.
4. When a book is returned by a user, it must be checked whether the user is a valid user,
and that the book is on the list of the books in the library and has been borrowed by
this user. If not, an appropriate message should be displayed on the screen. If the
request is a valid one, the stored information should be updated accordingly.
