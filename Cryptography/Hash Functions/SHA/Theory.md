# Secure Hash Algorithm (SHA)

## Introduction

The Secure Hash Algorithm (SHA) is a family of cryptographic hash functions designed by the National Security Agency (NSA) and published by the National Institute of Standards and Technology (NIST). SHA is widely used for securing data and verifying data integrity. The SHA family includes SHA-1, SHA-2, and SHA-3, with SHA-2 and SHA-3 being the most commonly used due to their strong security properties.

## Key Concepts

- **Hash Function**: A function that takes an input and produces a fixed-size string of bytes.
- **Digest**: The fixed-size output of a hash function.
- **Collision**: When two different inputs produce the same hash output.

## SHA Family

### SHA-1

- **Digest Size**: 160 bits
- **Security**: SHA-1 is no longer considered secure due to vulnerabilities to collision attacks.

### SHA-2

- **Variants**: SHA-224, SHA-256, SHA-384, SHA-512, SHA-512/224, SHA-512/256
- **Digest Sizes**: 224, 256, 384, 512 bits
- **Security**: SHA-2 is widely used and considered secure for most applications.

### SHA-3

- **Variants**: SHA3-224, SHA3-256, SHA3-384, SHA3-512
- **Digest Sizes**: 224, 256, 384, 512 bits
- **Security**: SHA-3 is the latest member of the SHA family and provides strong security with a different internal structure compared to SHA-2.

## How SHA Works

1. **Padding**:
   - The original message is padded so that its length is congruent to 448 modulo 512 (for SHA-1 and SHA-2) or 896 modulo 1024 (for SHA-512 variants). Padding is always added, even if the message length is already congruent to the required value.

2. **Appending Length**:
   - The length of the original message (before padding) is appended as a 64-bit integer (for SHA-1 and SHA-2) or a 128-bit integer (for SHA-512 variants).

3. **Initialization**:
   - SHA uses a set of initial hash values, which are specific constants.

4. **Processing**:
   - The padded message is processed in blocks (512-bit blocks for SHA-1 and SHA-2, 1024-bit blocks for SHA-512 variants). Each block goes through multiple rounds of operations involving bitwise logical functions, modular addition, and bitwise shifts/rotations.

5. **Output**:
   - The final output is the concatenation of the hash values, producing the fixed-size digest.

## Mathematical Background

### Bitwise Operations

SHA relies heavily on bitwise operations such as AND, OR, XOR, and NOT, as well as bitwise shifts and rotations.

### Modular Addition

Modular addition is used to combine the results of the bitwise operations with the message blocks and constants.

## Example (SHA-256)

1. **Padding**:
   - Original message: "abc"
   - Padded message: "abc" followed by padding bits to make the length congruent to 448 modulo 512.

2. **Appending Length**:
   - Append the length of the original message (24 bits for "abc") as a 64-bit integer.

3. **Initialization**:
   - Initialize hash values to specific constants.

4. **Processing**:
   - Process the padded message in 512-bit blocks through multiple rounds of operations.

5. **Output**:
   - Concatenate the hash values to produce the final 256-bit hash value.

## Security

The security of SHA-2 and SHA-3 relies on their complex combination of substitution, permutation, and mixing operations, which provide strong resistance against various cryptographic attacks.

### Key Size

SHA-2 and SHA-3 support multiple digest sizes, providing flexibility in security levels. Common digest sizes are 256 and 512 bits.

### Attacks on SHA

- **Collision Attack**: Attempts to find two different inputs that produce the same hash output. SHA-1 is vulnerable to collision attacks, but SHA-2 and SHA-3 are considered secure.
- **Preimage Attack**: Attempts to find an input that produces a specific hash output. SHA-2 and SHA-3 provide strong resistance against preimage attacks.
- **Length Extension Attack**: SHA-2 is vulnerable to length extension attacks, but this can be mitigated by using HMAC (Hash-based Message Authentication Code).

## Practical Considerations

- **Replacement of SHA-1**: Due to its vulnerabilities, SHA-1 has been largely replaced by SHA-2 and SHA-3 in most applications.
- **HMAC**: HMAC is commonly used with SHA-2 and SHA-3 to provide message integrity and authenticity.
- **Performance**: SHA-3 has a different internal structure compared to SHA-2, which may affect performance depending on the implementation.
