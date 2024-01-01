# Code-for-random-guess-number-game
Code for random guess number


#include <iostream>
#include <cstdlib>
#include <ctime>

int main() {
    // Seed for random number generation
    std::srand(std::time(0));

    // Generate a random number between 1 and 100
    int secretNumber = std::rand() % 100 + 1;

    int guess;
    int attempts = 0;

    std::cout << "Welcome to the Number Guessing Game!\n";

    do {
        std::cout << "Enter your guess: ";
        std::cin >> guess;
        attempts++;

        if (guess == secretNumber) {
            std::cout << "Congratulations! You guessed the correct number in " << attempts << " attempts.\n";
        } else if (guess < secretNumber) {
            std::cout << "Too low. Try again!\n";
        } else {
            std::cout << "Too high. Try again!\n";
        }

    } while (guess != secretNumber);

    return 0;
}
