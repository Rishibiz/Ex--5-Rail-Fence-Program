# Ex-5-Rail Fence Program
### Name : Rishi chandran R
### Reg No: 212223043005
# AIM:

To write a C program to implement the rail fence transposition technique.

# DESCRIPTION:

In the rail fence cipher, the plain text is written downwards and diagonally on successive "rails" of an imaginary fence, then moving up when we reach the bottom rail. When we reach the top rail, the message is written downwards again until the whole plaintext is written out. The message is then read off in rows.

# ALGORITHM:

### Step-1:Read the Plain text.
### Step-2: Arrange the plain text in row columnar matrix format.
### Step-3: Now read the keyword depending on the number of columns of the plain text.
### Step-4: Arrange the characters of the keyword in sorted order and the corresponding columns of the plain text.
### Step-5: Read the characters row wise or column wise in the former order to get the cipher text.

# PROGRAM
```
#include <stdio.h>
 #include <string.h>
 int main() {
 int i, j, k, l;
 char a[20], c[20], d[20];
 printf("\n\t\tRAIL FENCE TECHNIQUE\n");
 printf("\nEnter the input string: ");
 fgets(a, sizeof(a), stdin);
a[strcspn(a, "\n")] = '\0';
 l = strlen(a);
 for (i = 0, j = 0; i < l; i++) {
 if (i % 2 == 0) {
 c[j++] = a[i];
 }
 }
 for (i = 0; i < l; i++) {
 if (i % 2 == 1) {
 c[j++] = a[i];
 }
 }
 c[j] = '\0'; 
 printf("\nCipher text after applying rail fence: %s\n", c);
 if (l % 2 == 0) {
 k =l / 2;
 } else {
 k =(l / 2) + 1;
 }
 for (i = 0, j = 0; i < k; i++) {
 d[j] = c[i];
 j += 2;
 }
 for (i = k, j = 1; i < l; i++) {
d[j] = c[i];
 j += 2;
 }
 d[l] = '\0';
 printf("\nText after decryption: %s\n", d);
 return 0;
 }
```

# OUTPUT
![Screenshot 2025-04-07 081924](https://github.com/user-attachments/assets/fa0e2e18-c560-4dcd-8091-208538a886e7)


# RESULT
The program is executed successfully
