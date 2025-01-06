# Elliptic Curve Cryptography (ECC)

## Introduction

Elliptic Curve Cryptography (ECC) is a public-key cryptography approach based on the algebraic structure of elliptic curves over finite fields. ECC provides the same level of security as other public-key cryptosystems like RSA but with smaller key sizes, making it more efficient.

## Key Concepts

- **Elliptic Curve**: A set of points satisfying a specific mathematical equation.
- **Public Key**: A point on the elliptic curve, derived from the private key.
- **Private Key**: A randomly selected integer.
- **Base Point (G)**: A predefined point on the elliptic curve used in key generation.

## How ECC Works

1. **Elliptic Curve Equation**:
   - The general form of the elliptic curve equation is \( y^2 = x^3 + ax + b \) over a finite field \( \mathbb{F}_p \), where \( p \) is a prime number.

2. **Key Generation**:
   - Choose a private key \( d \), which is a random integer.
   - Compute the public key \( Q = dG \), where \( G \) is the base point on the elliptic curve and \( dG \) represents scalar multiplication.

3. **Encryption (Elliptic Curve Integrated Encryption Scheme - ECIES)**:
   - The sender generates a random integer \( k \) and computes the ephemeral public key \( R = kG \).
   - The shared secret is computed as \( S = kQ \), where \( Q \) is the recipient's public key.
   - The plaintext message \( M \) is encrypted using a symmetric encryption algorithm with a key derived from \( S \).

4. **Decryption**:
   - The recipient computes the shared secret \( S = dR \), where \( d \) is the recipient's private key and \( R \) is the ephemeral public key sent by the sender.
   - The symmetric key derived from \( S \) is used to decrypt the ciphertext.

## Mathematical Background

### Elliptic Curves

Elliptic curves are defined by the equation \( y^2 = x^3 + ax + b \) over a finite field. The set of points on the curve, along with a point at infinity, form an abelian group under a defined addition operation.

### Finite Fields

A finite field \( \mathbb{F}_p \) consists of a finite number of elements, where \( p \) is a prime number. Arithmetic operations in \( \mathbb{F}_p \) are performed modulo \( p \).

### Scalar Multiplication

Scalar multiplication involves multiplying a point \( G \) on the elliptic curve by an integer \( d \) to get another point on the curve. This operation is computationally efficient in one direction but difficult to reverse, providing the basis for ECC security.

## Example

1. **Elliptic Curve Parameters**:
   - Choose the elliptic curve \( y^2 = x^3 + 2x + 3 \) over \( \mathbb{F}_{97} \).
   - Choose the base point \( G = (3, 6) \).

2. **Key Generation**:
   - Alice chooses a private key \( d_A = 10 \).
   - Alice computes her public key \( Q_A = 10G = (80, 10) \).

3. **Encryption**:
   - Bob wants to send a message to Alice. He chooses a random integer \( k = 20 \).
   - Bob computes the ephemeral public key \( R = 20G = (46, 22) \).
   - Bob computes the shared secret \( S = 20Q_A = (52, 7) \).
   - Bob uses a symmetric encryption algorithm with a key derived from \( S \) to encrypt the message \( M \).

4. **Decryption**:
   - Alice receives \( R = (46, 22) \) and the ciphertext.
   - Alice computes the shared secret \( S = 10R = (52, 7) \).
   - Alice uses the symmetric key derived from \( S \) to decrypt the ciphertext and recover the message \( M \).

## Security

The security of ECC relies on the difficulty of the Elliptic Curve Discrete Logarithm Problem (ECDLP), which is the challenge of finding the integer \( d \) given the points \( G \) and \( Q = dG \).

### Key Size

ECC provides equivalent security to RSA with much smaller key sizes. For example, a 256-bit ECC key provides comparable security to a 3072-bit RSA key.

### Attacks on ECC

- **Side-Channel Attacks**: Exploit information leaked during the computation process, such as timing or power consumption.
- **Mathematical Attacks**: Attempt to solve the ECDLP directly, but are currently infeasible for properly chosen parameters.

## Practical Considerations

- **Curve Selection**: Use standardized curves like those recommended by NIST (e.g., P-256, P-384) to ensure security.
- **Implementation**: Ensure constant-time implementations to mitigate side-channel attacks.
- **Hybrid Encryption**: ECC is often used in combination with symmetric key cryptography for efficient encryption of large data.
