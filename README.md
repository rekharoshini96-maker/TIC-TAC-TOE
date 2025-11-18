#include <stdio.h>

int main()
{
    char ttt[9] = {' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' '};
    int pos;
    char move = 'X';

    for (int i = 1; i <= 9; i++)
    {
        printf("Enter your move: ");
        scanf("%d", &pos);

        ttt[pos] = move;      

        printf("%c|%c|%c\n", ttt[0], ttt[1], ttt[2]);
        printf("-+-+-\n");
        printf("%c|%c|%c\n", ttt[3], ttt[4], ttt[5]);
        printf("-+-+-\n");
        printf("%c|%c|%c\n", ttt[6], ttt[7], ttt[8]);

      
        if(
            (ttt[0]=='X' && ttt[1]=='X' && ttt[2]=='X') ||
            (ttt[3]=='X' && ttt[4]=='X' && ttt[5]=='X') ||
            (ttt[6]=='X' && ttt[7]=='X' && ttt[8]=='X') ||
            (ttt[0]=='X' && ttt[3]=='X' && ttt[6]=='X') ||
            (ttt[1]=='X' && ttt[4]=='X' && ttt[7]=='X') ||
            (ttt[2]=='X' && ttt[5]=='X' && ttt[8]=='X') ||
            (ttt[0]=='X' && ttt[4]=='X' && ttt[8]=='X') ||
            (ttt[2]=='X' && ttt[4]=='X' && ttt[6]=='X')
          )
        {
            printf("X wins\n");
            break;
        }

        
        if(move == 'X')
            move = 'O';
        else
            move = 'X';
    }

    return 0;
}
