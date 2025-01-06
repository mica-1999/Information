# Advanced Encryption Standard (AES)

## Introduction

The Advanced Encryption Standard (AES) is a symmetric encryption algorithm established by the U.S. National Institute of Standards and Technology (NIST) in 2001. It is widely used for securing data due to its efficiency and strong security properties.

## Key Concepts

- **Symmetric Encryption**: Uses the same key for both encryption and decryption.
- **Block Cipher**: Encrypts data in fixed-size blocks (128 bits for AES).
- **Key Size**: AES supports key sizes of 128, 192, and 256 bits.

## How AES Works

1. **Key Expansion**:
   - The original key is expanded into multiple round keys using the Rijndael key schedule.

2. **Initial Round**:
   - **AddRoundKey**: Each byte of the state is combined with a block of the round key using bitwise XOR.

3. **Main Rounds** (repeated 9, 11, or 13 times for 128, 192, or 256-bit keys):
   - **SubBytes**: Each byte in the state is replaced with its corresponding value from the S-box (a fixed substitution table).
   - **ShiftRows**: The rows of the state are shifted cyclically to the left.
   - **MixColumns**: The columns of the state are mixed using a linear transformation.
   - **AddRoundKey**: Each byte of the state is combined with a block of the round key using bitwise XOR.

4. **Final Round**:
   - **SubBytes**
   - **ShiftRows**
   - **AddRoundKey**

## Mathematical Background

### Galois Field (GF)

AES operates on bytes, which are elements of the finite field \( GF(2^8) \). Arithmetic operations in this field are performed modulo an irreducible polynomial.

### S-box

The S-box is a substitution table used in the SubBytes step. It is constructed by combining the multiplicative inverse in \( GF(2^8) \) with an affine transformation.

### MixColumns

The MixColumns step treats each column of the state as a polynomial over \( GF(2^8) \) and multiplies it by a fixed polynomial.

## Example

1. **Key Expansion**:
   - For a 128-bit key, the key is expanded into 11 round keys.

2. **Initial Round**:
   - The plaintext is XORed with the first round key.

3. **Main Rounds**:
   - For each round, the SubBytes, ShiftRows, MixColumns, and AddRoundKey steps are performed.

4. **Final Round**:
   - The SubBytes, ShiftRows, and AddRoundKey steps are performed (MixColumns is omitted).

## Security

The security of AES relies on its complex combination of substitution, permutation, and mixing operations, which provide strong resistance against various cryptographic attacks.

### Key Size

AES supports three key sizes: 128, 192, and 256 bits. Larger key sizes provide higher security but require more computational power.

### Attacks on AES

- **Brute-Force Attack**: Attempts to try all possible keys. Infeasible due to the large key space.
- **Side-Channel Attacks**: Exploit information leaked during the encryption process, such as timing or power consumption.
- **Cryptanalysis**: Attempts to find weaknesses in the algorithm. AES has been extensively analyzed and is considered secure when used correctly.

## Practical Considerations

- **Modes of Operation**: AES is often used with modes of operation like CBC (Cipher Block Chaining) or GCM (Galois/Counter Mode) to encrypt data larger than the block size.
- **Padding**: When encrypting data that is not a multiple of the block size, padding schemes like PKCS#7 are used to fill the remaining space.
- **Key Management**: Secure generation, storage, and distribution of keys are crucial for maintaining the security of AES.
