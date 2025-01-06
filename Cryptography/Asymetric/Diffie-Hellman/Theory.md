# Diffie-Hellman Key Exchange

## Introduction

The Diffie-Hellman key exchange is a method of securely exchanging cryptographic keys over a public channel. It was one of the first practical implementations of public key exchange and is widely used in various security protocols.

## Key Concepts

- **Public Parameters**: Two numbers, a prime \( p \) and a base \( g \), are agreed upon and shared publicly.
- **Private Key**: Each party generates a private key, which is kept secret.
- **Public Key**: Each party computes a public key from their private key and the public parameters.

## How Diffie-Hellman Works

1. **Public Parameters**:
   - Choose a large prime number \( p \).
   - Choose a base \( g \) (also known as the generator), where \( 1 < g < p \).

2. **Private and Public Keys**:
   - Each party generates a private key. Let's denote Alice's private key as \( a \) and Bob's private key as \( b \).
   - Each party computes their public key. Alice computes \( A = g^a \mod p \) and Bob computes \( B = g^b \mod p \).

3. **Key Exchange**:
   - Alice sends her public key \( A \) to Bob.
   - Bob sends his public key \( B \) to Alice.

4. **Shared Secret**:
   - Alice computes the shared secret as \( s = B^a \mod p \).
   - Bob computes the shared secret as \( s = A^b \mod p \).
   - Both computations result in the same shared secret \( s \) because \( B^a \mod p = (g^b \mod p)^a \mod p = g^{ba} \mod p \) and \( A^b \mod p = (g^a \mod p)^b \mod p = g^{ab} \mod p \).

## Mathematical Background

### Prime Numbers

Prime numbers are integers greater than 1 that have no positive divisors other than 1 and themselves. The security of Diffie-Hellman relies on the difficulty of computing discrete logarithms in a finite field defined by a large prime number.

### Modular Arithmetic

Modular arithmetic is a system of arithmetic for integers, where numbers "wrap around" after reaching a certain value, the modulus.

### Discrete Logarithm Problem

The discrete logarithm problem is the challenge of finding the exponent \( x \) in the equation \( g^x \equiv h \mod p \), given \( g \), \( h \), and \( p \). This problem is computationally hard, which underpins the security of Diffie-Hellman.

## Example

1. **Public Parameters**:
   - Choose \( p = 23 \) (a small prime for simplicity).
   - Choose \( g = 5 \).

2. **Private and Public Keys**:
   - Alice chooses a private key \( a = 6 \).
   - Bob chooses a private key \( b = 15 \).
   - Alice computes her public key \( A = 5^6 \mod 23 = 8 \).
   - Bob computes his public key \( B = 5^{15} \mod 23 = 19 \).

3. **Key Exchange**:
   - Alice sends \( A = 8 \) to Bob.
   - Bob sends \( B = 19 \) to Alice.

4. **Shared Secret**:
   - Alice computes the shared secret \( s = 19^6 \mod 23 = 2 \).
   - Bob computes the shared secret \( s = 8^{15} \mod 23 = 2 \).
   - Both Alice and Bob now share the secret \( s = 2 \).

## Security

The security of the Diffie-Hellman key exchange relies on the difficulty of solving the discrete logarithm problem. Even if an attacker knows the public parameters and the public keys, they cannot easily compute the shared secret without solving this problem.

### Key Size

The key size is typically measured in bits. Common key sizes are 2048, 3072, and 4096 bits. Larger key sizes provide higher security but require more computational power.

### Attacks on Diffie-Hellman

- **Man-in-the-Middle Attack**: An attacker intercepts the public keys and replaces them with their own, establishing separate shared secrets with each party.
- **Logjam Attack**: Exploits weaknesses in the implementation of the Diffie-Hellman key exchange to downgrade the security level.

## Practical Considerations

- **Ephemeral Diffie-Hellman (DHE)**: Uses temporary key pairs for each session to provide forward secrecy.
- **Elliptic Curve Diffie-Hellman (ECDH)**: Uses elliptic curve cryptography to provide the same level of security with smaller key sizes.
