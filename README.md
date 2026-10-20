# Computational Theory Assessment

**Name:** Oisin Forde  
**Student ID:** G00434079  
**Module:** Computational Theory  
**Language:** Python

## Overview

This repository contains my work for the Computational Theory assessment.

The project is developed using Python and Jupyter Notebook. The assessment explores concepts used by the SHA-256 hashing algorithm, including data representation, bitwise operations and the generation of SHA-256 constants.

The solutions, explanations, demonstrations and references are contained in `problems.ipynb`.

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

## Project Files

`problems.ipynb`  
Contains the assessment solutions, explanations, code and references.

`requirements.txt`  
Contains the Python packages required to run the project.

`README.md`  
Contains an overview of the repository and basic setup instructions.

## Requirements

The project uses Python, Jupyter Notebook and NumPy.

Install the required packages with:

```bash
pip install -r requirements.txt