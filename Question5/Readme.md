# 📚 Book Management Program in Java

This Java program demonstrates the use of **classes**, **objects**, and **arrays of objects**.  
It stores book information, displays books based on a condition, and calculates the **average price** of all books.

---

## 📌 Objectives

- Create a `Book` class with private data members
- Store multiple `Book` objects in an array
- Display books with price greater than 500
- Calculate and display the average book price
- Practice basic **Object-Oriented Programming (OOP)** concepts

---

## 🛠️ Technologies Used

- Java (JDK 8 or higher)
- Object-Oriented Programming (OOP)

---

## 📂 Project Structure

BookProgram/
│
├── Book.java
└── README.md

---

## ▶️ How to Run the Program

### 1️⃣ Compile the program

javac Book.java
### 2️⃣ Run the program
java Book
## 🧾 Source Code
~~~
public class Book {
    private int bookId;
    private String title;
    private double price;

    public Book(int bookId, String title, double price) {
        this.bookId = bookId;
        this.title = title;
        this.price = price;
    }

    public double getPrice() {
        return price;
    }

    public void display() {
        System.out.println("ID: " + bookId + ", Title: " + title + ", Price: " + price);
    }

    public static void main(String[] args) {
        Book[] books = new Book[5];
        books[0] = new Book(101, "Java Programming", 450);
        books[1] = new Book(102, "Data Structures", 650);
        books[2] = new Book(103, "Algorithms", 800);
        books[3] = new Book(104, "Web Development", 520);
        books[4] = new Book(105, "Database Systems", 390);

        System.out.println("Books with price greater than 500:");
        for (Book book : books) {
            if (book.getPrice() > 500) {
                book.display();
            }
        }

        double total = 0;
        for (Book book : books) {
            total += book.getPrice();
        }
        double average = total / books.length;

        System.out.println("\nAverage price: " + average);
    }
}
~~~
## 🧑‍💻 Sample Output
~~~
Books with price greater than 500:
ID: 102, Title: Data Structures, Price: 650.0
ID: 103, Title: Algorithms, Price: 800.0
ID: 104, Title: Web Development, Price: 520.0

Average price: 562.0
~~~
## 📘 Concepts Used
~~~
Class and Object
Constructor
Array of Objects
Encapsulation
Looping (for-each)
Conditional Statements
~~~
