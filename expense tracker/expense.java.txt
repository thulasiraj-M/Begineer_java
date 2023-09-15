import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

public class ExpenseTracker {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Double> expenses = new ArrayList<>();

        while (true) {
            System.out.println("1. Add Expense");
            System.out.println("2. Display Total Expenses");
            System.out.println("3. Exit");
            System.out.print("Enter your choice: ");
            int choice = scanner.nextInt();

            switch (choice) {
                case 1:
                    System.out.print("Enter the expense amount: ");
                    double expenseAmount = scanner.nextDouble();
                    expenses.add(expenseAmount);
                    System.out.println("Expense added successfully!");
                    break;
                case 2:
                    double totalExpenses = 0.0;
                    for (double expense : expenses) {
                        totalExpenses += expense;
                    }
                    System.out.println("Total Expenses: " + totalExpenses);
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