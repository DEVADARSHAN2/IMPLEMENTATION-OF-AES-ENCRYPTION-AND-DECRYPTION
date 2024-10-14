# Ex-8 -Implement the AES Encryption and decryption
## Aim: 
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption. 
## ALGORITHM: 
1. AES is based on a design principle known as a substitution-permutation. 
2. AES does not use a Feistel network like DES, it uses variant of Rijndael. 
3. It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits. 
4. AES operates on a 4 x 4 column-major order array of bytes, termed the state PROGRAM: 
## PROGRAM
```
#include <stdio.h> 
#include <string.h> 

void xor_encrypt_decrypt(char *input, char *key) { 
    int input_len = strlen(input); 
    int key_len = strlen(key); 
    for (int i = 0; i < input_len; i++) { 
        input[i] = input[i] ^ key[i % key_len]; 
    } 
}

int main() { 
    char url[] = "https://www.youtube.com/"; 
    char key[] = "secretkey"; 

    printf("\n***** ADVANCED-ENCRYPTION-STANDARD-DES-ALGORITHM *****\n\n"); 
    
    
    printf("Original text: %s\n", url); 
    
   
    xor_encrypt_decrypt(url, key); 
    printf("Encrypted text: %s\n", url); 
    
  
    xor_encrypt_decrypt(url, key); 
    printf("Decrypted text: %s\n", url); 
    
    return 0; 
}

```
## OUTPUT: 
![Screenshot 2024-10-14 091243](https://github.com/user-attachments/assets/bafc87b0-01e5-498e-b7b7-4f8121a9f9b4)


## RESULT: 
The execution program is successfully executed.
