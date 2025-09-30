# 📑 Presentation: Hill Cipher Implementation (3x3 Key Matrix)

## Hill Cipher Encryption & Decryption
   A classical cryptography algorithm using linear algebra


## 🔹Introduction :
- Hill Cipher invented by Lester S. Hill (1929)

- Polygraphic substitution cipher (works on blocks of letters, not individual letters)

- Uses matrix multiplication modulo 26

- Requires invertible key matrix for decryption


## 🔹Working Principle :
1. Represent letters as numbers:
a=0, b=1, ..., z=25

2. Break plaintext into blocks of size n (here 3)

3. Multiply block vector by key matrix (mod 26) → ciphertext

4. For decryption: Multiply ciphertext by inverse key matrix (mod 26)


## 🔹Encryption Flow (Code Part 1) :
