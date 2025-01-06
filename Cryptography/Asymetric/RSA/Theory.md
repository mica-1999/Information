# RSA Cryptography

## Introduction

RSA (Rivest-Shamir-Adleman) is one of the first public-key cryptosystems and is widely used for secure data transmission. It is based on the mathematical fact that it is easy to multiply large numbers together, but difficult to factor their product back into the original prime numbers.

## Key Concepts

- **Public Key**: Used for encrypting messages. It is shared openly.
- **Private Key**: Used for decrypting messages. It is kept secret.
- **Modulus (n)**: The product of two large prime numbers, used in both the public and private keys.
- **Public Exponent (e)**: An integer used as part of the public key.
- **Private Exponent (d)**: An integer used as part of the private key, calculated from the public exponent.

## How RSA Works

1. **Key Generation**:
   - Choose two distinct large prime numbers, \( p \) and \( q \).
   - Compute \( n = pq \). \( n \) is used as the modulus for both the public and private keys.
   - Compute the totient \( \phi(n) = (p-1)(q-1) \).
   - Choose an integer \( e \) such that \( 1 < e < \phi(n) \) and \( e \) is coprime with \( \phi(n) \). \( e \) is the public exponent.
   - Determine \( d \) as \( d \equiv e^{-1} \mod \phi(n) \). \( d \) is the private exponent.

2. **Encryption**:
   - The sender converts the plaintext message \( M \) into an integer \( m \) such that \( 0 \leq m < n \).
   - The ciphertext \( c \) is computed as \( c \equiv m^e \mod n \).

3. **Decryption**:
   - The receiver computes \( m \equiv c^d \mod n \).
   - The plaintext message \( M \) is then recovered from \( m \).

## Mathematical Background

### Prime Numbers

Prime numbers are integers greater than 1 that have no positive divisors other than 1 and themselves. The security of RSA relies on the difficulty of factoring large prime numbers.

### Modular Arithmetic

Modular arithmetic is a system of arithmetic for integers, where numbers "wrap around" after reaching a certain value, the modulus.

### Euler's Totient Function

Euler's Totient Function \( \phi(n) \) is used to determine the number of integers up to \( n \) that are coprime with \( n \). For two distinct primes \( p \) and \( q \), \( \phi(n) = (p-1)(q-1) \).

## Example

1. **Key Generation**:
   - Choose \( p = 61 \) and \( q = 53 \).
   - Compute \( n = 61 \times 53 = 3233 \).
   - Compute \( \phi(n) = (61-1)(53-1) = 3120 \).
   - Choose \( e = 17 \) (common choice).
   - Compute \( d \equiv 17^{-1} \mod 3120 = 2753 \).

2. **Encryption**:
   - Convert plaintext message \( M \) to integer \( m \). Suppose \( m = 65 \).
   - Compute ciphertext \( c \equiv 65^{17} \mod 3233 = 2790 \).

3. **Decryption**:
   - Compute \( m \equiv 2790^{2753} \mod 3233 = 65 \).
   - Recover plaintext message \( M = 65 \).

## Security

The security of RSA relies on the practical difficulty of factoring the product of two large prime numbers. As computing power increases, the key sizes must also increase to ensure security.

### Key Size

The key size is typically measured in bits. Common key sizes are 1024, 2048, and 4096 bits. Larger key sizes provide higher security but require more computational power.

### Attacks on RSA

- **Factoring Attack**: Attempts to factor the modulus \( n \) into its prime components \( p \) and \( q \).
- **Timing Attack**: Exploits the time taken to perform decryption operations to gain information about the private key.
- **Chosen Ciphertext Attack**: The attacker can choose a ciphertext and obtain its decryption under an unknown key.

## Practical Considerations

- **Padding Schemes**: To prevent certain attacks, padding schemes like OAEP (Optimal Asymmetric Encryption Padding) are used.
- **Hybrid Encryption**: RSA is often used in combination with symmetric key cryptography to encrypt large amounts of data efficiently.
