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

### Functions used :
- ``` keyMatrixMaker(key) ``` → converts key string → 3×3 numeric matrix
  
- ```matrixMultiplier(a,b)``` → multiplies key matrix with message vector

- ```listOrdConverter(l)``` → converts message to numbers (ord - 97)

- ```matrixInverseChecker(m)``` → ensures matrix is invertible


## 🔹Encryption Example :
- Key entered: ```"abcdefghi"```
  → Key Matrix =
  ```
     [0 1 2]
     [3 4 5]
     [6 7 8]
   ```
- Plaintext: ```"meetme"``` → padded → ```"meetmez"```

- Ciphertext = transformed message (mod 26)


## 🔹Decryption Flow (Code Part 2) :

### Additional Functions:
- ```matrixTranspose(m)```

- ```matrixCofactor(m)```

- ```matrixAdjoint(m)```

- ```matrixDeterminant(m)```

- ```multiplicativeInverse(num)``` → modular inverse under mod 26

- ```matrixInverse(m)``` → inverse of key matrix modulo 26

### Steps:
1. Compute inverse key matrix mod 26

2. Convert ciphertext into numeric blocks

3. Multiply each block with inverse key matrix

4. Convert numbers back → plaintext


## 🔹Important Conditions :
- Key must form a non-singular matrix (determinant ≠ 0 mod 26)

- Otherwise, inverse does not exist → decryption impossible

- Padding ensures all blocks are of size 3


## 🔹Demo Output ;
### Encryption Example:
```
  Key: "mathcipher"
  Message: "hillcipher"
  Encrypted: "lbxvfw..."
```

### Decryption Example: 
```
Encrypted: "lbxvfw..."
Decrypted: "hillcipher"
```















