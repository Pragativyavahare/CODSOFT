package atmif;
import java.util.Scanner;
public class atm {



		
		 private double balance;

		    public atm(double initialBalance) {
		        this.balance = initialBalance;
		    }

		    public double getBalance() {
		        return balance;
		    }

		    public void deposit(double amount) {
		        if (amount > 0) {
		            balance += amount;
		            System.out.println("Deposit successful. New balance: $" + balance);
		        } else {
		            System.out.println("Invalid deposit amount.");
		        }
		    }

		    public boolean withdraw(double amount) {
		        if (amount > 0 && amount <= balance) {
		            balance -= amount;
		            System.out.println("Withdrawal successful. New balance: $" + balance);
		            return true;
		        } else {
		            System.out.println("Insufficient funds or invalid amount.");
		            return false;
		        }
		    } 
		
		
		    private atm account;
		    private Scanner scanner;

		    public atm(atm account) {
		        this.account = account;
		        this.scanner = new Scanner(System.in);
		    }

		    public void start() {
		        boolean running = true;

		        while (running) {
		            displayMenu();
		            int choice = getUserChoice();

		            switch (choice) {
		                case 1:
		                    checkBalance();
		                    break;
		                case 2:
		                    performDeposit();
		                    break;
		                case 3:
		                    performWithdrawal();
		                    break;
		                case 4:
		                    running = false;
		                    System.out.println("Exiting. Thank you for using the ATM.");
		                    break;
		                default:
		                    System.out.println("Invalid option. Please try again.");
		            }
		        }

		        scanner.close();
		    }

		    private void displayMenu() {
		        System.out.println("\nATM Menu:");
		        System.out.println("1. Check Balance");
		        System.out.println("2. Deposit");
		        System.out.println("3. Withdraw");
		        System.out.println("4. Exit");
		        System.out.print("Select an option: ");
		    }

		    private int getUserChoice() {
		        while (!scanner.hasNextInt()) {
		            System.out.println("Invalid input. Please enter a number.");
		            scanner.next(); // consume invalid input
		        }
		        return scanner.nextInt();
		    }

		    private void checkBalance() {
		        System.out.println("Current balance: $" + account.getBalance());
		    }

		    private void performDeposit() {
		        System.out.print("Enter deposit amount: ");
		        double depositAmount = getValidAmount();
		        if (depositAmount > 0) {
		            account.deposit(depositAmount);
		        } else {
		            System.out.println("Invalid deposit amount.");
		        }
		    }

		    private void performWithdrawal() {
		        System.out.print("Enter withdrawal amount: ");
		        double withdrawalAmount = getValidAmount();
		        if (withdrawalAmount > 0) {
		            account.withdraw(withdrawalAmount);
		        } else {
		            System.out.println("Invalid withdrawal amount.");
		        }
		    }

		    private double getValidAmount() {
		        while (!scanner.hasNextDouble()) {
		            System.out.println("Invalid input. Please enter a valid amount.");
		            scanner.next(); // consume invalid input
		        }
		        return scanner.nextDouble();
		    }

		    public static void main(String[] args) {
		        atm account = new atm(500.00); // Initial balance
		        atm atm = new atm(account);
		        atm.start();
		    }
		}
