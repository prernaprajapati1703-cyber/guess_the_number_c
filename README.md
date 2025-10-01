# guess_the_number_c
“A simple C program for Guess the Number game.”



	#include <stdio.h>
    #include <stdlib.h>
    #include <time.h>

int main() {
    // Initialize random number generator
    srand(time(0));

    // Generate random number between 1 and 100
    int randomNumber = (rand() % 100) + 1;
    int guessed, no_of_guesses = 0;

    // Guessing loop
    do {
        printf("Guess the number (1 to 100): ");
        scanf("%d", &guessed);
        no_of_guesses++;

        if (guessed > randomNumber) {
            printf("Lower number please!\n");
        } else if (guessed < randomNumber) {
            printf("Higher number please!\n");
            
        } else {
            printf("🎉 Congratulations! You guessed the number in %d attempts.\n", no_of_guesses);
        }

    } while (guessed != randomNumber);

    return 0;

}
