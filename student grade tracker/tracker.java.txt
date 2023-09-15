import java.util.Scanner;

public class GradeTracker {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        
        System.out.print("Enter the number of students: ");
        int numStudents = input.nextInt();
        
        String[] names = new String[numStudents];
        double[] grades = new double[numStudents];
        
        for (int i = 0; i < numStudents; i++) {
            System.out.print("Enter the name of student " + (i + 1) + ": ");
            names[i] = input.next();
            
            System.out.print("Enter the grade of student " + (i + 1) + ": ");
            grades[i] = input.nextDouble();
        }
        
        System.out.println("\nGrade Report:");
        for (int i = 0; i < numStudents; i++) {
            System.out.println(names[i] + ": " + grades[i]);
        }
        
        input.close();
    }
}