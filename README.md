# number-guessing
ITs a number guessing game 

(We will write a program that generates a random number and asks the player to guess
it. If the player?s guess is higher than the actual number, the program displays ?Lower
number please?. Similarly, if the user?s guess is too low, the program prints ?Higher
number please?).


#include <stdio.h>
#include <conio.h>

int main()
{
    srand(time(0));
    int randomnumber = (rand()%100)+1;
    int no_of_guesses = 0;
    int guessed;
    
    do
    {
        printf("Guess the number");
        scanf("%d", &guessed);
        if(guessed>randomnumber)
        {
            printf("lower number please!\n");
            
        }
        else if(randomnumber<guessed)
        {
            printf("higher number please!\n");
        }
        else
        {
            printf("congrats!!\n");
        }
        no_of_guesses++;
    }
    while(guessed!=randomnumber);
    printf("you gussed the number in %d guesses", no_of_guesses);
    
    return 0;
}
