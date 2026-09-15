---
layout: project
type: project
image: img/micromouse/RSP2.png
title: "Rock, Paper, Sciccors"
date: 2024
published: true
labels:
  - video games 
  - C
summary: "My ICS 212 rock, paper, scissors interactive game"
---

<img class="img-fluid" src="../img/micromouse/RPS.png.jpg">

This is one of my first C-based projects that I created during my time in ICS 212. My interactive text-based game for rock paper scissors used user inputs, random generation, & score keeping. Calling on CompTurn() and the while statement allows for the game's functionality. While the player makes decisions based off the printInstruct() function. 

Throughout a series of choices & turns, the tallied and scored total was computed from the calcWinner(comp, user) function.  Resulting in the output of the winner being 'u' for user, 'c' for computer, & 't' for tie. Otherwise, the program would determine that the user misrepresented or mistyped their response, and the console would allow for entering another value. 


Below is a code segment from my project:

<hr>
  
```cpp

void printInstruct(void);
int  CompTurn(void);    
int calcWinner(int, int);

int main(void){

     //random seeding 
     srand(time(NULL));
     char user = 'a';
     int comp; 
     int input = 0;
     int winner; 
     int userScore = 0, compScore = 0, tieScore = 0; 

    while(user != EOF){
         printInstruct();
         user = getchar();    
         if (user != EOF){
            getchar();
            printf("User entered %c\n", user);
            comp = CompTurn();
            printf("Computer Chose %c\n", comp);
            winner = calcWinner(comp, user);
                while (input > 0){
                    if (winner == 'u'){
                        userScore++;
                    } else if (winner == 'c') {
                        compScore++;
                        printf("You have chosen to quit\n");
                    } else if (winner == 't') {
                        tieScore++;
                    } else {
                        printf("Invalide option");
                    }
                }
            
             printf("Got %c\n", winner);

         } else {  
            printf("You have chosen to quit\n");
            printf("thank you for playing\n");
            printf("Here is the total score\n");
            
            printf("Computer wins: %c\n", compScore);
            printf("user wins: %c\n", userScore);
            printf("ties: %c\n", tieScore);
        } 
    }
    return 0;
} 

```

<hr>
