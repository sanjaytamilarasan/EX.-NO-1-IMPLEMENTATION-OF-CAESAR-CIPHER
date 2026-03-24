# EX. NO: 1 : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```c
#include <stdio.h>

int main()
{
    char text[100];
    int key, i;

    printf("Enter a message: ");
    scanf("%[^\n]", text);

    printf("Enter key (shift value): ");
    scanf("%d", &key);

    // Encrypt
    for (i = 0; text[i] != '\0'; i++)
    {
        if (text[i] >= 'A' && text[i] <= 'Z')
            text[i] = ((text[i] - 'A' + key) % 26) + 'A';
        else if (text[i] >= 'a' && text[i] <= 'z')
            text[i] = ((text[i] - 'a' + key) % 26) + 'a';
    }
    printf("Encrypted: %s\n", text);

    // Decrypt
    for (i = 0; text[i] != '\0'; i++)
    {
        if (text[i] >= 'A' && text[i] <= 'Z')
            text[i] = ((text[i] - 'A' - key + 26) % 26) + 'A';
        else if (text[i] >= 'a' && text[i] <= 'z')
            text[i] = ((text[i] - 'a' - key + 26) % 26) + 'a';
    }
    printf("Decrypted: %s\n", text);

    return 0;
}
```
## OUTPUT:
<img width="664" height="259" alt="image" src="https://github.com/user-attachments/assets/295e3423-a161-43c6-9825-0f4ffa3b70cb" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
