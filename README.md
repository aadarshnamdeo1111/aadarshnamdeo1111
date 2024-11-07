 include<stdio.h>
 2 #include<conio.h>
 3 int you,Computer; global value
 4 int menu()
 5 {
 6    int ch;
 7    printf("\n1. Select Rock");
 8    printf("\n2. Select Paper");
 9    printf("\n3. Select Scissor");
 10    printf("\n4. Exist");
 11    printf("\n Enter your choice");
 12    scanf("%d",&ch);
 13      return ch;
 14       }
 15       void setup(){
 16           label:
 17       Computer=rand()%4;
 18       if(Computer 0)
 19        goto label;
 20 
21        you=menu();
 22        }
 23       void MakeLogic(){
 24       switch(you)
 25       {
 26           case 1
 27               if(Computer 1)//// you=rock,Computer=rock
 28               {printf("\nGame Draw");
 29                   printf("\nyou=rock\nComputer=rock");
 30               }
 31               else if(Computer 2)//// you=rock,Computer=paper
 32               {
 33                   printf("\nComputer Won");
 34                   printf("\nyou=rock\nComputer=paper");
 35               }
 36               else you=rock,Computer=scissor
 37               {
 38                   printf("\nYou Won");
 39                   printf("\nyou=rock\nComputer=scissor");
 40               }
 41               break;
 42           case 2
 43               if(Computer 1)//// you=paper,Computer=rock
 44               {
 45                   printf("\nYou Won");
 46                   printf("\nyou=paper\nComputer=rock")  }
 48               else if(Computer 2)//// you=paper,Computer=paper
 49               {
 50                   printf("\nGame Draw")    printf("\nyou=paper\nComputer=paper");
 52               }
 53               else you=paper,Computer=scissor
 54               {
 55                   printf("\nComputer Won");
 56                   printf("\nyou=paper\nComputer=scissor");
 57               }
 58               break;
 59           case 3
 60               if(Computer 1)//// you=scissor,Computer=rock
 61               {
 62                   printf("\nComputer Won");
 63                   printf("\nyou=scissor\nComputer=rock");
 64               }
 65               else if(Computer 2)//// you=scissor,Computer=paper
 66               {
 67                   printf("\nYou Won");
 68                   printf("\nyou=scissor\nComputer=paper");
 69               }
 70               else you=scissor,Computer=scissor
 71               {
 72                   printf("\nGame Draw");
 73                   printf("\nyou=scissor\nComputer=scissor");
 74               }
 75               break;
 76           case 4
 77             exit(0);
 78           default:
 79            printf("\nInvalid user choice")     }
 81      }
 82 int main ()
 83 {
 84    while(1)
 85    {
 86     system("cls");
 87        setup();
 88   MakeLogic();
 89   getch();
 90    }
 91 return 0
