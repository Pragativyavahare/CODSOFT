package CALCI;
import java.util.Scanner;

public class ScoreCalculator {

	public static void main(String[] args) {
		
		        Scanner scanner = new Scanner(System.in);
		        
		        // Assuming 5 subjects for this example
		        final int totalsubjects = 6;
		        
		        // Array to store marks obtained in each subject
		        int[] marks = new int[totalsubjects];
		        
		        // Prompt user to enter marks for each subject
		        System.out.println("Enter marks obtained in each subject (out of 100):");
		        for (int i = 0; i < totalsubjects; i++) {
		            System.out.print("Subject " + (i + 1) + ": ");
		            marks[i] = scanner.nextInt();
		        }
		        
		        // Calculate total marks
		        int totalMarks = 0;
		        for (int mark : marks) {
		            totalMarks += mark;
		        }
		        
		        // Calculate average percentage
		        double averagePercentage = (double) totalMarks / totalsubjects;
		        
		        // Determine grade based on average percentage
		        char grade;
		        if (averagePercentage >= 85) {
		            grade = 'A';
		        } else if (averagePercentage >= 75) {
		            grade = 'B';
		        } else if (averagePercentage >= 65) {
		            grade = 'C';
		        } else if (averagePercentage >= 55) {
		            grade = 'D';
		        } else {
		            grade = 'F';
		        }
		        
		     // Display results in a structured format.
		        System.out.println("\nResults:");
		        System.out.println("Total Marks: " + totalMarks);
		        System.out.printf("Average Percentage: %.2f%%\n", averagePercentage);
		        System.out.println("Grade: " + grade);

		        
		        scanner.close();
		    }
		}
