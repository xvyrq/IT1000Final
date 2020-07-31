# Past Projects


1. *RanchTools*  
This was a program I originally wrote for a friend to calculate his profit from sales on different platforms.
I ended up making a number of additions to it after that and was quite pleased with how it turned out given my
very limited experience in C at the time. It was the first time I'd messed around with a login of any sort and 
so it's obviously not the most advanced system but I was quite proud of myself when it was complete.
```
#include <stdio.h>
#include <string.h>
#include <stdlib.h>

void Login(void);
void ProfitCalc(void);
void Motivation(void);
void ChefLevel(void);

int main(void) {
    
int input1;

Login();

do {
    do {

    printf("\n--Welcome to the Ranch Mainframe--\n");
    printf("Select any option or enter 4 to exit\n");
        
        printf("1. Profit Calculator\n"); 
        printf("2. Motivation\n");
        printf("3. Chef Level\n");
        printf("4. Exit Program\n");
        scanf("%d", &input1);
    
    if(!(input1 > 0 && input1 < 5))
        printf("\n***Please enter selection from 1-4***\n");
    else
    break;
    }while(1);

    switch(input1){

        case 1:
            ProfitCalc();
            break;

        case 2:
            Motivation();
            break;
                    
        case 3: 
            ChefLevel();
            break;
        
        case 4:
            printf("\nGoodbye!\n");
            exit(0);
            break;

} }while(input1 != 4);
}

void Login(void) {

    char user[20];
    char pswd[20];

        printf("\nPlease enter username: ");
            scanf("%s", user);

        printf("\nPlease enter password: ");
            scanf("%s", pswd);

        if(strcmp(user, "ranch") == 0 && strcmp(pswd, "default") == 0) {

            printf("\n--ACCESS GRANTED--\n");  }

        else printf("\n--ACCESS DENIED--\n"); }


void ProfitCalc(void) {

int sellingplat, level;
double paid, sold, P, ship;

do {
    printf("\n***Please select your selling platform***\n");
    printf("1. GOAT\n");
    printf("2. StockX\n");
    printf("3. eBay\n");
    printf("4. Exit Program\n");
    scanf("%d", &sellingplat);
    if(!(sellingplat > 0 && sellingplat < 5))
        printf("\n***Please enter selection from 1-4***\n");
    else
    break;
    }while(1);

    switch(sellingplat) {

        case 1: do {

                printf("\nPrice Bought For = $");
                    scanf("%lf", &paid);

                printf("\nPrice Sold For = $");
                    scanf("%lf", &sold);

                P = (sold - paid) * .905 - 5;
                printf("\nProfit = $%.2f\n", P);
        break;
        }while(1);

        case 2: do {

                printf("\nPrice Bought For = $");
                    scanf("%lf", &paid);
                
                printf("\nPrice Sold For = $");
                    scanf("%lf", &sold);

                printf("\nWhat Level Seller are you? ");
                scanf("%d", &level);

                if(!(level > 0 && level < 5))
                    printf("\n***Please enter selection from 1-4***\n");
                else
                break;
                }while(1);
                
                if(level==1) {
                    P = (sold - paid) * .875; }
                
                else if(level==2) {
                    P = (sold - paid) * .880; }

                else if(level==3) {
                    P = (sold - paid) * .885; }

                else if(level==4) {
                    P = (sold - paid) * .890; }

                printf("\nProfit = $%.2f\n", P);
                break;

        case 3: do {

                printf("\nPrice Bought For = $");
                    scanf("%lf", &paid);

                printf("\nPrice Sold For = $");
                    scanf("%lf", &sold);

                printf("\nShipping Cost = $");
                    scanf("%lf", &ship);

                P = (sold - paid - ship) * .875;

                printf("Profit = $%.2f\n", P);
                break;
                }while(1);
                
        case 4: do {

                printf("\nGoodbye!\n");
                exit(0);
                break;
                }while(1);

        default: do {

                printf("\n---ERROR---INCORRECT INPUT---\n");
                break;
                }while(1);
    }}


void Motivation(void) {

int Z;

do {
    printf("\nEnter a number 1-10 for a motivational quote or enter 0 to exit program\n");
        scanf("%d", &Z);

    if(Z==1) {
        printf("\nWith a new day comes new strength and new thoughts.\n"); }

    else if(Z==2) {
        printf("\nSetting goals is the first step in turning the invisible into the visible.\n"); }

    else if(Z==3) {
        printf("\nQuality is not an act, it is a habit.\n"); }

    else if(Z==4) {
        printf("\nWell done is better than well said.\n"); }

    else if(Z==5) {
        printf("\nKnowing is not enough; we must apply. Willing is not enough; we must do.\n"); }

    else if(Z==6) {
        printf("\nGood, better best. Never let it rest. 'Til your good is better and your better is best.\n"); }

    else if(Z==7) {
        printf("\nOptimism is the faith that leads to achievement. Nothing can be done without hope and confidence.\n"); }

    else if(Z==8) {
        printf("\nThe secret of getting ahead is getting started.\n"); }

    else if(Z==9) {
        printf("\nIt does not matter how slowly you go as long as you don't stop.\n"); }

    else if(Z==10) {
        printf("\nYesterday is not ours to recover, but tomorrow is ours to win or lose.\n"); }
    
    else if(Z==0) {
        printf("\nGoodbye!\n");
        exit(0); }

    break;
    }while(1);
    }


void ChefLevel(void) {

int sales;

do {
        printf("\nHow many sales do you have in the last month?\n");

            printf("\n0. Exit Program");
            printf("\n1. 0-10 Sales");
            printf("\n2. 11-25 Sales");
            printf("\n3. 26-50 Sales");
            printf("\n4. 51+ Sales\n");
                scanf("%d", &sales);

            if(sales==1) {
                printf("\nYou are Mole. Congrats.\n"); }
            
            else if(sales==2) {
                printf("\nYou better get a job at Sabai homie.\n"); }

            else if(sales==3) {
                printf("\nYou making decent money lil guy.\n"); }

            else if(sales==4) {
                printf("\nYou a chef wit three Michelin Stars.\n"); }
            
            else if(sales==0) {
                printf("\nGoodbye!\n");
                exit(0); }
            break;
            }while(1);
            }   
```
2. *MadLibs*  
This one is extremely basic but helped me first learn how to use basic `printf` and `scanf` functions. 

  ```
  #include <stdio.h>  
  #include <stdlib.h>
  
  int main()
  {
  char color[20];
  char pluralNoun[20];
  char celebrityF[20];
  char celebrityL[20];
  
  printf("Enter a color: ");
  scanf("%s", color);
  
  printf("Enter a plural noun: ");
  scanf("%s", pluralNoun);
  
  printf("I love %s %s\n", celebrityF, celebrityL);
  
  return 0;
  }
  ```
