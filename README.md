# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

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
#include <ctype.h> 
 
int main() { 
    char name[100], encrypted[100], decrypted[100]; 
    int i, key = 3; 
 
    printf("Enter your name: "); 
    scanf(" %[^\n]", name); 
 
    for (i = 0; name[i] != '\0'; i++) { 
        if (isupper(name[i])) 
            encrypted[i] = (name[i] - 'A' + key) % 26 + 'A'; 
        else if (islower(name[i])) 
            encrypted[i] = (name[i] - 'a' + key) % 26 + 'a'; 
        else 
            encrypted[i] = name[i]; 
    } 
    encrypted[i] = '\0'; 
 
    printf("Encrypted name: %s\n", encrypted); 
 
    for (i = 0; encrypted[i] != '\0'; i++) { 
        if (isupper(encrypted[i])) 
            decrypted[i] = (encrypted[i] - 'A' - key + 26) % 26 + 'A'; 
        else if (islower(encrypted[i])) 
            decrypted[i] = (encrypted[i] - 'a' - key + 26) % 26 + 'a'; 
        else 
            decrypted[i] = encrypted[i]; 
    } 
    decrypted[i] = '\0'; 
 
    printf("Decrypted name: %s\n", decrypted); 
 
    return 0; 
}
```
## OUTPUT:

<img width="783" height="244" alt="image" src="https://github.com/user-attachments/assets/e5776d62-3a00-4ec0-961a-3a367b170e11" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
