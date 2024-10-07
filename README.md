# numberguessinggame
Number Guessing Game A simple console-based game implemented in C. The player must guess a randomly generated number between 0 and 9, receiving hints for each guess.  Features 1.Random number generation 2.Feedback on guesses 3.Unlimited attempts
code:
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int number, usernumber;
    srand(time(NULL));
    number = rand() % 10;

    while (1) {
        printf("Guess a number between 0-9.\n");
        printf("Enter your guess: ");
        scanf("%d", &usernumber);

        if (usernumber > number) {
            printf("Number is less than %d. Try again.\n\n", usernumber);
        } else if (usernumber < number) {
            printf("Number is greater than %d. Try again.\n\n", usernumber);
        } else {
            printf("You are right!\n");
            break;
        }
    }

    return 0;
}

