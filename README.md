# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

# NAME: Karthikeyan
# REG.NO: 212224040152

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main() {
    char plaintext[100], encrypted[100], decrypted[100];
    int key, i;

    printf("Enter the Plain Text: ");
    fgets(plaintext, sizeof(plaintext), stdin);

    printf("Enter the Key value: ");
    scanf("%d", &key);
    for (i = 0; plaintext[i] != '\0'; i++) {
        if (plaintext[i] >= 'A' && plaintext[i] <= 'Z') {
            encrypted[i] = ((plaintext[i] - 'A' + key + 26) % 26) + 'A';
        }
        else if (plaintext[i] >= 'a' && plaintext[i] <= 'z') {
            encrypted[i] = ((plaintext[i] - 'a' + key + 26) % 26) + 'a';
        }
        else {
            encrypted[i] = plaintext[i];
        }
    }
    encrypted[i] = '\0';
    
    for (i = 0; encrypted[i] != '\0'; i++) {
        if (encrypted[i] >= 'A' && encrypted[i] <= 'Z') {
            decrypted[i] = ((encrypted[i] - 'A' - key + 26) % 26) + 'A';
        }
        else if (encrypted[i] >= 'a' && encrypted[i] <= 'z') {
            decrypted[i] = ((encrypted[i] - 'a' - key + 26) % 26) + 'a';
        }
        else {
            decrypted[i] = encrypted[i];
        }
    }
    decrypted[i] = '\0';

    printf("\nPlain Text     : %s", plaintext);
    printf("Encrypted Text : %s", encrypted);
    printf("Decrypted Text : %s", decrypted);

    return 0;
}

```
## OUTPUT:
<img width="1916" height="937" alt="image" src="https://github.com/user-attachments/assets/b5729d4c-d28e-4ff4-92eb-64be31299954" />



## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
