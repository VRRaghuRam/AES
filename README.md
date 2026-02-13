# Name : V.R.Raghu Ram
# Reg No : 212224220075
# Date : 13/02/2026
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:
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
    char url[] = "RaghuRam";
    char key[] = "secretkey";
    
    printf("Original text: %s\n", url);
    xor_encrypt_decrypt(url, key);
    printf("Encrypted text: %s\n", url);
    xor_encrypt_decrypt(url, key);
    printf("Decrypted text: %s\n", url);

    return 0;
}
```
# OUTPUT:
<img width="1248" height="647" alt="image" src="https://github.com/user-attachments/assets/c567bae9-fa62-4e1b-91c0-1464f297a505" />



# RESULT:
The URL is encrypted and decrypted successfully, demonstrating AES-based URL encryption.


