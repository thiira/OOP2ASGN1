# OOP2ASGN1
import java.util.Scanner;

public class LoginProgram {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String correctUsername = "user123";
        String correctPassword = "pass123";
        int maxAttempts = 3;
        int attempts = 0;

        while (attempts < maxAttempts) {
            System.out.print("Enter username: ");
            String username = scanner.nextLine();
            System.out.print("Enter password: ");
            String password = scanner.nextLine();

            if (username.equals(correctUsername) && password.equals(correctPassword)) {
                System.out.println("Login successful!");
                break;
            } else {
                System.out.println("Incorrect username or password. Please try again.");
                attempts++;
            }

            if (attempts < maxAttempts) {
                System.out.println("You have " + (maxAttempts - attempts) + " attempts remaining.\n");
            } else {
                System.out.println("Sorry, you have reached the maximum number of attempts. Account locked.");
            }
        }

        scanner.close();
    }
}
