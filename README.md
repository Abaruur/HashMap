# HashMap
**Storing Custom Class objects in Array List**
Collection classes are used to store built in objects such as Integer, String, and Character etc. But the potential of collection classes isn't just restricted to the storage of built-in objects. Collections classes can store any similar type of objects, be it objects of a built-in class or objects of a user-defined class. This feature of collection class is very useful when we are making an application which requires us to store many objects of user-defined classes and not just objects of built-in classes.

public class Book {
    // HashMap Example. Create Book Cass.
    int id;
    String name,author, publisher;
    int quantity;

    public Book (int id, String name, String author, String publisher, int quantity)
    {
        this.id = id;
        this.name = name;
        this.author = author;
        this.publisher = publisher;
        this.quantity = quantity;
    }
}


++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

import java.util.HashMap;
import java.util.Map;

public class BookMainMethod {
    //Create a Class for Entry point in java and define main method.
    public static void main(String[] args) {
        HashMap<Integer, Book> map = new HashMap<Integer, Book>();
        //Creating Books
        Book b1 = new Book(101, "Death Note", "Do not know", "BPB", 800);
        Book b2 = new Book(102, "Data communication & networking", "Forouzan", "Mc Graw Hill", 400);
        Book b3 = new Book(103, "Operating Sys", "Willey", "Galvin", 600);
        //Adding books to map
        map.put(1, b1);
        map.put(2, b2);
        map.put(3, b3);

        //Transversing map

        for (Map.Entry<Integer, Book> entry : map.entrySet()) {
            int key = entry.getKey();
            Book b = entry.getValue();
            System.out.println(key + " Details:");
            System.out.println(b.id + " " + b.name + " " + b.author + " " + b.publisher + " " + b.quantity);
        }
    }
}
