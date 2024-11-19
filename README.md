# Affine Bigram Cipher Analysis

This repository contains the implementation of the cryptanalysis of the affine bigram substitution cipher. The project demonstrates the use of frequency analysis and modular arithmetic to decrypt ciphertexts encrypted using this cipher.

## Overview
Affine bigram cipher encrypts text by dividing it into bigrams (pairs of characters) and applying the following transformation:
\[ Y_i = (a \cdot X_i + b) \mod m^2 \]
where:
- \( X_i \) and \( Y_i \) are numerical representations of plaintext and ciphertext bigrams.
- \( a \) and \( b \) are the cipher keys.
- \( m \) is the alphabet size.

Decryption is achieved using the modular inverse:
\[ X_i = a^{-1} \cdot (Y_i - b) \mod m^2 \]

## Features
- **Frequency Analysis**: Identifies the most frequent bigrams in the ciphertext.
- **Modular Arithmetic**: Solves linear congruences to find possible keys.
- **Decryption**: Applies candidate keys to decrypt the ciphertext.
- **Validation**: Automatically filters decrypted texts using statistical measures (e.g., Index of Coincidence).

## Getting Started

### Prerequisites
- Python 3.8 or newer
- Required Python libraries:
  - `pandas`
  - `openpyxl`
