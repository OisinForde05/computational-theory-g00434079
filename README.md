# Computational Theory Assessment

**Name:** Oisin Forde  
**Student ID:** G00434079  
**Module:** Computational Theory  
**Language:** Python

## Overview

This repository contains my work for the Computational Theory assessment.

The project is developed using Python and Jupyter Notebook and explores the main components of the SHA-256 hashing algorithm. The assessment covers data representation, bitwise operations, constant generation, message padding and parsing, the compression function, and a complete SHA-256 implementation.

The solutions, explanations, demonstrations, tests and references are contained in `problems.ipynb`.

## Progress

### Problem 1 - Representing SHA-256 Data

Investigates how different types of SHA-256 data can be represented in Python, including:

- 32-bit words
- Sequences of 32-bit words
- Input messages
- 512-bit message blocks
- Final 256-bit hash values
- Big-endian integers

### Problem 2 - SHA-256 Bitwise Operations

Implements the Boolean and bitwise functions used by SHA-256:

- `Ch(x, y, z)`
- `Maj(x, y, z)`
- `Sigma0(x)`
- `Sigma1(x)`
- `sigma0(x)`
- `sigma1(x)`

Basic checks are used to verify the functions return the expected results.

### Problem 3 - Generating the SHA-256 Constants

Generates the 64 SHA-256 round constants by:

- Generating the first 64 prime numbers
- Calculating their cube roots
- Extracting the fractional parts
- Multiplying the values by $2^{32}$
- Converting the results to unsigned 32-bit integers
- Displaying the constants in hexadecimal
- Comparing the generated values with FIPS 180-4

All 64 generated constants are compared against the values given in the Secure Hash Standard.

### Problem 4 - Padding and Parsing Messages

Implements the SHA-256 message padding and parsing process, including:

- Recording the original message length in bits
- Appending the required `1` bit
- Adding zero padding
- Storing the original message length as a 64-bit big-endian integer
- Splitting padded messages into 512-bit blocks
- Parsing each block into sixteen 32-bit words
- Testing important padding boundary cases

### Problem 5 - SHA-256 Compression Function

Implements the main SHA-256 compression process, including:

- Building the 64-word message schedule
- Initialising the SHA-256 working variables
- Performing the 64 compression rounds
- Calculating `T1` and `T2`
- Updating the hash state after each block

### Problem 6 - Complete SHA-256 Implementation

Combines the previous components into a complete SHA-256 implementation.

The final `sha256(msg)` function:

- Accepts a message as bytes
- Processes every padded message block
- Updates the hash state after each block
- Returns a 64-character lowercase hexadecimal digest
- Is tested against Python's `hashlib.sha256`

## Project Files

`problems.ipynb`  
Contains the assessment solutions, explanations, demonstrations, tests and references.

`requirements.txt`  
Contains the Python packages required to run the notebook.

`README.md`  
Contains an overview of the project and setup instructions.

`.gitignore`  
Defines files and folders that should not be committed to the repository.

`AGENTS.md`  
Contains repository guidance for coding agents.

## Requirements

The project uses:

- [Python](https://www.python.org/)
- [Jupyter Notebook](https://jupyter.org/)
- [NumPy](https://numpy.org/)

Install the required packages with:

```bash
pip install -r requirements.txt
```

## Running the Project

Clone the repository:

```bash
git clone https://github.com/OisinForde05/computational-theory-g00434079.git
```

Move into the project directory:

```bash
cd computational-theory-g00434079
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Open the notebook:

```bash
jupyter notebook problems.ipynb
```

Run the notebook cells from top to bottom.

Before submission, the notebook should be checked using **Restart Kernel and Run All Cells** to confirm that it executes successfully from a clean state.

## References

The main sources used throughout the project are:

- [NIST FIPS 180-4 - Secure Hash Standard](https://nvlpubs.nist.gov/nistpubs/FIPS/NIST.FIPS.180-4.pdf)
- [Ian McLoughlin - Computational Theory](https://github.com/ianmcloughlin/computational-theory)
- [Python Documentation](https://docs.python.org/3/)
- [NumPy Documentation](https://numpy.org/doc/)
