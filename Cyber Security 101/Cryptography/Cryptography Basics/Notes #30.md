## Section 1 Plaintext to Ciphertext

**Plaintext** is the original, readable message or data before it’s encrypted.

**Ciphertext** is the scrambled, unreadable version of the message after encryption.

**Cipher** is an algorithm or method to convert plaintext into ciphertext and back again. 

**Key** is a string of bits the cipher uses to encrypt or decrypt data. 

**Encryption** is the process of converting plaintext into ciphertext using a cipher and a key.

**Decryption** is the reverse process of encryption.

## Questions

**What do you call the encrypted plaintext?**
Answer: **Ciphertext**

**What do you call the process that returns the plaintext?**

Answer: **Decryption**

## Section 2 Historical Ciphers

The idea is to shift each letter by a certain number to encrypt the message.

For encryption, we shift to the right (of the alphabet) by the key, and to decrypt, we shift to the left by the key.

Question: 

**Knowing that XRPCTCRGNEI was encrypted using Caesar Cipher, what is the original plaintext?**

Ans: Using a key of 15 to decrypt, we get the answer **"ICENCRYPT"**

## Section 3 Types of Encryption

There are two primary types:

1: **Symmetric Encryption**

Symmetric encryption uses the same key to encrypt and decrypt the data, therefore communicating the key to the intended parties is challenging incase of the presence of an adversary the failure to protect the key will give access to the senders vital data.

Examples of symmetric encryption include: 

1. DES: Data encryption standard. Adopted in 1977. Uses a 56 bit key. DES was successfully broken in 24 Hours leading to the creation of 3DES.

2. 3DES: Applies DES 3 times. Key size is 168 bits. 3DES was replaced by AES and deprecated in 2019. 

3. AES: Advanced Encryption Standard,  Adopted in 2001. Key size can vary from 128, 192 and 256 bits.

2: **Asymmetric Encryption**

Asymmetric encryption uses a pair of keys, one to encrypt and the other to decrypt. Also called Public Key Cryptography.

Asymmetric encryption tends to be slower, and many asymmetric encryption ciphers use larger keys than symmetric encryption.

Examples are RSA, Diffie-Hellman, and Elliptic Curve cryptography (ECC). The two keys involved in the process are referred to as a public key and a private key.

## Questions:

**Should you trust DES? (Yea/Nay)**
Ans: **Nay**

**When was AES adopted as an encryption standard?**
Ans: **2001**

## Section 4 Basic Math

Modern Cryptography lies in Mathematics. 2 Mathematical operations used are, 
1. XOR Operation
2. Modulo Operation

**XOR Operation**

Short for exclusive OR, Is a logical operator in binary arithmetic. XOR compares 2 Binary digits and returns 1 if they are different and 0 if they are similar.

A	B	A ⊕ B
0	0	0
0	1	1
1	0	1
1	1	0

**Modulo Operation**

Another mathematical operation we often encounter in cryptography is the modulo operator, commonly written as % or as mod. The modulo operator, X%Y, is the remainder when X is divided by Y.

E.g: 25%5 = 0 because 25 divided by 5 is 5, with a remainder of 0, i.e., 25 = 5 × 5 + 0

# Questions:

1. **What’s 1001 ⊕ 1010?**
Ans: 0011

2. **What’s 118613842%9091?**
Ans: 3,565
(Multiply the division of 118613842%9091=13,047, by the divisor=9,091, and subtract the difference from the dividend=118,613,842. To recieve the answer)

3. **What’s 60%12?**
Ans: 0
