import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

public class LibraryManagementSystem {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
       // Scanner s = new Scanner(System.in);
        
        List<String> books = new ArrayList<>();

        while (true) {
            System.out.println("1. Add Book");
            System.out.println("2. Display Books");
            System.out.println("3. Exit");
            System.out.print("\nEnter your choice: ");
            int choice = scanner.nextInt();

            switch (choice) {
                case 1:
                    System.out.print("Enter the book name: ");
                   String bookName=scanner.nextLine();
                   bookName+=scanner.nextLine();
                   // String bookName = scanner.readLine().split(" ");
                    books.add(bookName);
                    System.out.println("Book added successfully!");
                    break;
                case 2:
                    System.out.println("List of books:\n");
                    for (String book : books) {
                        System.out.println(book);
                    }
                    System.out.println("\n");
                    break;
                case 3:
                    scanner.close();
                    System.exit(0);
                    break;
                default:
                    System.out.println("Invalid choice. Please try again.");
                    break;
            }
        }
    }
}