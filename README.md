## EX. NO: 1 : IMPLEMENTATION OF CAESAR CIPHER
 
## AIM:

To implement the simple substitution technique named Caesar cipher using C language.

## DESCRIPTION:

To encrypt a message with a Caesar cipher, each letter in the message is changed using a simple rule: shift by three. Each letter is replaced by the letter three letters ahead in the alphabet. A becomes D, B becomes E, and so on. For the last letters, we can think of the
alphabet as a circle and "wrap around". W becomes Z, X becomes A, Y bec mes B, and Z
becomes C. To change a message back, each letter is replaced by the one three before it.

## EXAMPLE:

![image](https://github.com/Hemamanigandan/CNS/assets/149653568/eb9c6c43-8c80-4cdd-b9d4-91705a311c79)


## ALGORITHM:

### STEP-1: Read the plain text from the user.
### STEP-2: Read the key value from the user.
### STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.
### STEP-4: Else subtract the key from the plain text.
### STEP-5: Display the cipher text obtained above.


## PROGRAM :-

```
Name: Ramya R
Reg No: 212223230169
```
``` 
#include <stdio.h> 
#include <string.h> 
void encrypt(char message[], int shift)  
{ 
char ch; 
for (int i = 0; message[i] != '\0'; ++i)  
{ 
        ch = message[i]; 
        if (ch >= 'a' && ch <= 'z')  
        { 
            ch = ch + shift; 
            if (ch > 'z')  
            { 
                ch = ch - 'z' + 'a' - 1; 
            } 
            message[i] = ch; 
        }  
        else if (ch >= 'A' && ch <= 'Z')  
        { 
            ch = ch + shift; 
            if (ch > 'Z')  
           { 
                ch = ch - 'Z' + 'A' - 1; 
            } 
            message[i] = ch; 
        } 
    } 
    printf("Encrypted message: %s\n", message); 
} 
void decrypt(char message[], int shift)  
{ 
    char ch; 
    for (int i = 0; message[i] != '\0'; ++i)  
    { 
        ch = message[i]; 
        if (ch >= 'a' && ch <= 'z')  
        { 
            ch = ch - shift; 
            if (ch < 'a')  
            { 
                ch = ch + 'z' - 'a' + 1; 
            } 
            message[i] = ch; 
        }  
        else if (ch >= 'A' && ch <= 'Z')  
        { 
            ch = ch - shift; 
            if (ch < 'A')  
            { 
                ch = ch + 'Z' - 'A' + 1; 
            } 
            message[i] = ch; 
        } 
    } 
    printf("Decrypted message: %s\n", message); 
} 
int main()  
{ 
    char message[100]; 
    int shift; 
    printf("Enter a message: "); 
    gets(message);   
  
    printf("Enter shift amount: "); 
    scanf("%d", &shift); 
    char encrypted_message[100]; 
    strcpy(encrypted_message, message); 
encrypt(encrypted_message, shift); 
decrypt(encrypted_message, shift); 
return 0; 
}
```


## OUTPUT :-
![image](https://github.com/user-attachments/assets/6f1942c3-1820-4b2d-91d7-3f70da1bbfa2)

## RESULT:

The program is executed successfully. 

