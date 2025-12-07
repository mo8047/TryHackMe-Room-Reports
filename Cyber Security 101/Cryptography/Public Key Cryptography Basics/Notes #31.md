## Section 1

Authentication: You want to be sure you communicate with the right person, not someone else pretending.

Authenticity: You can verify that the information comes from the claimed source.

Integrity: You must ensure that no one changes the data you exchange.

Confidentiality: You want to prevent an unauthorized party from eavesdropping on your conversations.

## Section 2
# Common Use of Asymmetric Encryption

Asymmetric encryption is relatively slow compared to symmetric encryption, that is why we use asymmetric encryption to agree on symmetric encryption ciphers and keys.

## Section 3
# RSA

RSA is a public-key encryption system built on the difficulty of factoring huge numbers.

Encrypt with the public key (n, e), decrypt with the private key (n, d).

Security comes from multiplying two huge primes (which is easy) versus factoring their product (which is extremely hard).

Example workflow: choose primes p and q → compute n = p·q and ϕ(n) → choose e (public exponent) → compute d (private exponent).

Encryption: c = m^e mod n. Decryption: m = c^d mod n.

In CTFs, RSA challenges often give some combination of p, q, n, e, d, m, c, and you must reconstruct the missing values or decrypt the ciphertext.

Tools like RsaCtfTool and rsatool help break weak RSA setups quickly.

# Questions 
1: **Knowing that p = 4,391 and q = 6,659. What is n?**
Answer: 4,391*6,659 = **23,239,669**

2: **Knowing that p = 4391 and q = 6659. What is ϕ(n)?**
Answer: 23,239,669-4,391-6,659+1 = **29,228,620**

## Section 4
# Diffie-Hellman Key Exchange

Key exchange aims to establish a shared secret between two parties. It is a method that allows two parties to establish a shared secret over an insecure communication
channel without requiring a pre-existing shared secret and without an observer being able to get this key

**Scenario**

Person 1 and 2 agree on a **p** and ***g** value of 29 and 3: These values will serve as the public facing values.
Now Person 1 and 2 have to chose a secret number that when calculated with the p and g values will result in the same values for both parties.

Assuming Person 1 picks **13** so **a=13** and person 2 picks **15** so **b=15**

So person 1 sends A=g^a mod p; = A=3^13 mod 29 = 19
and person 2 sends B=g^b mod p; = B=3^15 mod 29 = 26

Therefore **A=19** adn **B=26**

To find the key now we have to follow this format.
key = B^a mod p = **26^13 mod 29 = 10**
key = A^b mod p = **19^15 mod 29 = 10**

# Questions
1: Consider p = 29, g = 5, a = 12. What is A?

A = g^a mod p; **5^12 mod 29 = 7**

2: Consider p = 29, g = 5, b = 17. What is B?

B = g^b mod p; **5^17 mod 29 = 9**

3: Knowing that p = 29, a = 12, and you have B from the second question, what is the key calculated by Bob? (key = Ba mod p)

Key = B^a mod p; **9^12 mod 29 = 24**

4: Knowing that p = 29, b = 17, and you have A from the first question, what is the key calculated by Alice? (key = Ab mod p)

Key = A^b mod p; **7^17 mod 29 = 24**
