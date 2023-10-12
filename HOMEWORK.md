# 6. **Homework #08**

## Objective:

Your task is to create a Java program that simulates a simple book catalog. The program should allow the user to perform various actions like adding a new book, removing an existing book, and finding books based on different criteria such as the author, title, or year of publication.

## Requirements

### 1. Use `ArrayList` to Store Book Objects
Start by defining a `Book` class with fields like `title`, `author`, and `yearOfPublication`. Use an `ArrayList` to store these book objects.

**Code Example for ArrayList:**

import java.util.ArrayList;
import java.util.List;

public class BookCatalog {
List<Book> books = new ArrayList<>();

    // Methods for adding, removing, and finding books will go here
}

### 2. Sort Books Using Lambda Expressions and `Comparator`
Implement functionality to sort the books by different fields—title, author, or year of publication—using lambda expressions and the `Comparator` interface.

**Code Example for Comparator:**

books.sort(Comparator.comparing(Book::getTitle));

### 3. Use Stream API for Filtering and Manipulating the Catalog
Implement methods that allow the user to filter books by different criteria using the Stream API.

**Code Example for Stream API:**
List<Book> booksByAuthor = books.stream()
.filter(book -> "Some Author".equals(book.getAuthor()))
.collect(Collectors.toList());

## Bonus Tasks

### Bonus 1: Average Rating
For those who wish to go the extra mile, implement a feature to find the average rating of books by a particular author using the Stream API's `average()` method.

### Bonus 2: Flattening Nested Collections
Use the `flatMap` method to flatten nested collections, like a list of all tags across all books.
---