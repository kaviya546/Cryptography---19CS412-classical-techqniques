## HILL CIPHER
Hill cipher using with diffrent key values
### AIM:
To develop a simple C program to implement Hill Cipher.
### DESIGN STEPS:
### Step 1:
Design of Hill Cipher algorithnm
### Step 2:
Implementation using C or pyhton code
### Step 3:
Testing algorithm with different key values.

### ALGORITHM DESCRIPTION:
```

  * The Hill cipher is a substitution cipher invented by Lester S. Hill in 1929. Each letter is
represented by a number modulo 26. To encrypt a message, each block of n letters is
multiplied by an invertible n × n matrix, again modulus 26.
  * To decrypt the message, each block is multiplied by the inverse of the matrix used for
encryption. The matrix used for encryption is the cipher key, and it should be chosen randomly
from the set of invertible n × n matrices (modulo 26).
  * The cipher can, be adapted to an alphabet with any number of letters. All arithmetic just needs
to be done modulo the number of letters instead of modulo 26.
```
### PROGRAM:
#include <stdio.h>
int main()
{
unsigned int key[3][3] = {{6, 24, 1}, {13, 16, 10}, {20, 17, 15}};
unsigned int inverseKey[3][3] = {{8, 5, 10}, {21, 8, 21}, {21, 12, 8}};
char msg[4];
unsigned int enc[3] = {0}, dec[3] = {0};
printf("Enter plain text: ");
scanf("%3s", msg);
for (int i = 0; i < 3; i++)
for (int j = 0; j < 3; j++)
enc[i] += key[i][j] * (msg[j] - 'A') % 26;
printf("Encrypted Cipher Text: %c%c%c\n", enc[0] % 26 + 'A', enc[1] % 26 + 'A', enc[2
for (int i = 0; i < 3; i++)
for (int j = 0; j < 3; j++)
dec[i] += inverseKey[i][j] * enc[j] % 26;
printf("Decrypted Cipher Text: %c%c%c\n", dec[0] % 26 + 'A', dec[1] % 26 + 'A', dec[2
The program is executed successfully
return 0;
}
###  OUTPUT:
![WhatsApp Image 2025-03-19 at 08 16 29_0691a1b8](https://github.com/user-attachments/assets/989efad8-9cfe-4568-bea0-98c050fa24f4)
### Result :
The program executed successfully.

