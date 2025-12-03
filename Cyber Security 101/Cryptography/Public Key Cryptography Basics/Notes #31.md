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
