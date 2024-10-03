# Cryptography---19CS412-classical-techqniques
## Register Number : 212223040088
## Name : KARTHIKEYAN M

# Caeser Cipher
Caeser Cipher using with different key values

# AIM:

To develop a simple C program to implement Caeser Cipher.

## DESIGN STEPS:

### Step 1:

Design of Caeser Cipher algorithnm 

### Step 2:

Implementation using C code

### Step 3:

Testing algorithm with different key values. 

## PROGRAM:
```
#include <stdio.h>
#include <ctype.h>
#include <string.h>

char ALPHABET[] = "abcdefghijklmnopqrstuvwxyz";

void encrypt(char* text, int shift) {
    for (int i = 0; text[i] != '\0'; i++) {
        if (isalpha(text[i])) {
            int index = tolower(text[i]) - 'a';
            text[i] = ALPHABET[(index + shift) % 26];
        }
    }
}

void decrypt(char* text, int shift) {
    encrypt(text, -shift);
}

int main() {
    char choice[10];
    char text[100];
    int shift;
    printf("Do you want to encrypt or decrypt? ");
    scanf("%s", choice);
    printf("Enter the text: ");
    scanf("%s", text);
    printf("Enter the shift: ");
    scanf("%d", &shift);

    if (strcmp(choice, "encrypt") == 0) {
        encrypt(text, shift);
        printf("Encrypted text: %s\n", text);
    } else if (strcmp(choice, "decrypt") == 0) {
        decrypt(text, shift);
        printf("Decrypted text: %s\n", text);
    } else {
        printf("Invalid choice.\n");
    }

    return 0;
}
```
## OUTPUT:
## Encryption:
![Screenshot (473)](https://github.com/ashmistalin/Ceaser_cipher/assets/103128410/1625b02f-588c-46e7-9073-8451412bf4fe)

## Decryption:
![Screenshot (474)](https://github.com/ashmistalin/Ceaser_cipher/assets/103128410/dc0d29b1-b4ef-4c69-9ad8-ae0210e72526)

## RESULT:
The program is executed successfully

---------------------------------

