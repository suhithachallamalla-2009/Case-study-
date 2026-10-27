
#include <stdio.h>

int main()
{
    int choice;
    float balance, amount;

    printf("Enter current account balance: ");
    scanf("%f", &balance);

    printf("\nATM MENU\n");
    printf("1. Balance Inquiry\n");
    printf("2. Cash Withdrawal\n");
    printf("3. Cash Deposit\n");

    printf("Enter your choice: ");
    scanf("%d", &choice);

    if (choice == 1)
    {
        printf("Current Balance = %.2f\n", balance);
    }
    else if (choice == 2)
    {
        printf("Enter withdrawal amount: ");
        scanf("%f", &amount);

        if (amount > 0 && amount <= balance)
        {
            balance = balance - amount;
            printf("Transaction successful\n");
            printf("Remaining Balance = %.2f\n", balance);
        }
        else
        {
            printf("Insufficient balance\n");
        }
    }
    else if (choice == 3)
    {
        printf("Enter deposit amount: ");
        scanf("%f", &amount);

        if (amount > 0)
        {
            balance = balance + amount;
            printf("Deposit successful\n");
            printf("Updated Balance = %.2f\n", balance);
        }
        else
        {
            printf("Invalid deposit amount\n");
        }
    }
    else
    {
        printf("Invalid option\n");
    }
    
}
