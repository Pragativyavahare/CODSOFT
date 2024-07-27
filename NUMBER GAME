package GAME;
import java.util.Random;
import java.util.Scanner;

public class NGG {

	public static void main(String[] args) {
		

		
		
		        Scanner scanner = new Scanner(System.in);
		        Random random = new Random();
		        int numberofround = 1;

		        while (true) {
		            int guessedNumber = random.nextInt(100) + 1;
		            int attemptsLeft = 10;
		            boolean hasCorrectlyGuessed = false;

		            System.out.println("\nRound " + numberofround);
		            System.out.println("Hello,I have generated a number between 1 and 100. Can you guess it?");

		            while (attemptsLeft > 0) {
		                System.out.print("You have " + attemptsLeft + " attempts left. Enter your next guess: ");
		                int guess = scanner.nextInt();

		                if (guess < 1 || guess > 100) {
		                    System.out.println("Please guess a number between 1 and 100.");
		                    continue;
		                }

		                attemptsLeft--;

		                if (guess < guessedNumber) {
		                    System.out.println("Too low!");
		                } else if (guess > guessedNumber) {
		                    System.out.println("Too high!");
		                } else {
		                    System.out.println("Great Job! You guessed the correct number.");
		                    hasCorrectlyGuessed = true;
		                    break;
		                }
		            }

		            if (!hasCorrectlyGuessed) {
		                System.out.println("Sorry, you've used all your attempts. The correct number was " + guessedNumber + ".");
		            }

		            System.out.print("Do you want to play another round? (yes/no): ");
		            String playAgain = scanner.next().trim().toLowerCase();
		            if (!playAgain.equals("yes")) {
		                System.out.println("Thanks for playing!");
		                break;
		            } else {
		                numberofround++;
		            }
		        }

		        scanner.close();
		    }
		}
