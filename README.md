// "# First-Assignmnet-of-C-language" 
// Name: Abdul Rehman
// S/o:  Muhammad Qasim Kakar
// Roll No: 49,   BS(CS)


#include <stdio.h>

int isprime(int num) {
    int i;

    // Check if the number is divisible by any number from 2 to (num-1)
    for (i = 2; i < num; i++) {
        if (num % i == 0) {
            return 0; // Not a prime number
        }
    }

    return 1; // Prime number
}

int main() {
    int num, retry = 1;

    while (retry) {
        printf("Enter a number between 2 and 100: ");
        scanf("%d", &num);

        if (num >= 2 && num <= 100) {
            if (isprime(num)) {
                printf("%d is a prime number.\n", num);
            } else {
                printf("%d is not a prime number.\n", num);
            }

            retry = 0;
        } else {
            printf("Number out of range. Press 1 to try again.\n");
            scanf("%d", &retry);
        }
    }

    return 0;
}
