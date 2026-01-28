# Question 5 : Object Interaction & Array of Objects

## Book.java

### Code:
```
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
```