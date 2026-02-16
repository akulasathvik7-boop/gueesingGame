# gueesingGame
//using random prefined class importing from util .class

import java.util.Random;
import java.util.Scanner;

public class GuessingGame {
    public static void main(String[] args) {
        // Create a Scanner object to read user input
        Scanner scanner = new Scanner(System.in);
        // Create a Random object to generate random numbers
        Random random = new Random();

        // Generate a random number between 1 and 100 (inclusive)
        int secretNumber = random.nextInt(100) + 1;
        int attempts = 0;
        int guess;
        boolean guessedCorrectly = false;

        System.out.println("Welcome to the Number Guessing Game!");
        System.out.println("I have selected a number between 1 and 100. Try to guess it!");

        // Loop until the user guesses correctly
        while (!guessedCorrectly) {
            System.out.print("Enter your guess: ");
            guess = scanner.nextInt();
            attempts++;

            if (guess < secretNumber) {
                System.out.println("Too low! Try again.");
            } else if (guess > secretNumber) {
                System.out.println("Too high! Try again.");
            } else {
                System.out.println("Congratulations! You guessed the number in " + attempts + " attempts.");
                guessedCorrectly = true;
            }
        }

        // Close the scanner to prevent resource leaks
        scanner.close();
    }
}
this is my first github repository
<br>
Author-sathik varma
