# Hill Cipher Encryption and Decryption (for 3×3 matrix)
This repository contains a Python implementation of the Hill Cipher encryption and decryption algorithm.

The Hill Cipher is a polygraphic substitution cipher based on linear algebra that operates on blocks of letters at a time, each letter represented by a number modulo 26, and using a key matrix of size n×n.
In this implementation, a 3×3 key matrix is used, which means the plaintext is processed in blocks of 3 letters. The implementation is done purely in Python, without relying on external libraries for matrix calculations.

## 📖 Introduction
This code was developed as part of a college project to gain a deeper understanding of:
Matrix operations (multiplication, determinant, adjoint, inverse)

Modular arithmetic (mod 26 for the alphabet)

Classical cryptography techniques
The objective was to implement the Hill Cipher encryption and decryption algorithm from scratch, without using external libraries or predefined matrix functions.

Through this project, I explored the fundamental concepts behind the Hill Cipher and gained practical experience in combining mathematics with cryptography in Python.

## 🛠 How does the program work?
### 1.Key Matrix Creation
The key string (length 9 or padded) is converted into numbers (a=0, b=1, ..., z=25).

These numbers are reshaped into a 3×3 key matrix.

### 2.Encryption
The plaintext is split into blocks of 3.

Each block is multiplied by the key matrix under modulo 26.

The resulting numbers are converted back to letters to form ciphertext.

### 3.Decryption
The determinant of the key matrix is computed modulo 26.

Its multiplicative inverse is found.

Using the adjoint and inverse determinant, the inverse matrix is built.

Ciphertext blocks are multiplied with the inverse matrix modulo 26 to recover the original plaintext.


## ▶️ Usage
### 1.Clone the repository
git clone https://github.com/YourUsername/HillCipher_3x3.git
cd HillCipher_3x3

