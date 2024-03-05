import java.util.Scanner;

public class TextAdventureGame {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Welcome to the Text-based Adventure Game!");

        // Start the game
        playGame(scanner);

        // Close the scanner
        scanner.close();
    }

    private static void playGame(Scanner scanner) {
        System.out.println("You find yourself in a mysterious land. Choose your path wisely.");

        // Game loop
        while (true) {
            System.out.println("\n1. Go left");
            System.out.println("2. Go right");
            System.out.println("3. Stay where you are");

            // Get user input
            int choice = getUserChoice(scanner);

            // Process user choice
            switch (choice) {
                case 1:
                    System.out.println("You chose to go left. You encounter a friendly creature.");
                    // Add more story and decision points here
                    break;
                case 2:
                    System.out.println("You chose to go right. You stumble upon a mysterious cave.");
                    // Add more story and decision points here
                    break;
                case 3:
                    System.out.println("You chose to stay where you are. Nothing eventful happens.");
                    // Add more story and decision points here
                    break;
                default:
                    System.out.println("Invalid choice. Please choose again.");
            }
        }
    }

    private static int getUserChoice(Scanner scanner) {
        // Handle user input and ensure it's a valid integer
        while (!scanner.hasNextInt()) {
            System.out.println("Invalid input. Please enter a number.");
            scanner.next(); // Consume the invalid input
        }
        return scanner.nextInt();
    }
}
